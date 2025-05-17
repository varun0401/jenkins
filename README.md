Jenkins Job Creation: Implementing Version Control in Your CI/CD Pipeline

1.Creating the Jenkins Job

Opened Jenkins and clicked on “New Item”. Created a Freestyle project and named it Newitem. Under the Source Code Management section, selected Git. Entered my GitHub repository URL: https://github.com/varun0401/jenkins Changed the branch specification from master to main, since my GitHub repo uses main as the default branch.

Adding Build Steps
In the Build section, I added a Windows batch command. I used the following command to simulate a simple build: echo "Building the project..." This command was added in the “Execute Windows batch command” section and used to verify that Jenkins executes the build step after cloning the repository.

Running the Build and Output
Clicked Build Now to trigger the build manually. Viewed the logs under Console Output, which showed the following:

![WhatsApp Image 2025-05-17 at 23 22 53_d138627d](https://github.com/user-attachments/assets/6eefcea9-741e-4e26-a0f8-eb07407e81c3)


This confirmed that Jenkins successfully: Fetched the code from GitHub Checked out the correct commit Executed the batch command Finished the build successfully

Challenges Faced and Solution

I initially got an error: “Couldn't find any revision to build.” This happened because Jenkins was looking for the master branch, which didn’t exist in my GitHub repo. I resolved it by changing the branch specifier in Jenkins to main.

![WhatsApp Image 2025-05-17 at 23 11 02_b6db7569](https://github.com/user-attachments/assets/e732390e-edd5-4988-8188-a091c435617c)
