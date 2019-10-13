# :computer: Developer Onboarding Guide #

## Prerequisites ##

Add your SSH key to your Bitbucket account so that you don't have to keep typing your username and password for each git push.

1. Copy your public SSH key
    * `cat ~/.ssh/id_rsa.pub`
    * Copy the output of this command.

2. From Bitbucket, choose **Bitbucket settings** from your avatar in the lower left. The **Account settings** page opens.

3. Under the **Security** section, click **SSH keys.**

4. Click the **Add key** button.

5. Paste your key.
![key box](https://confluence.atlassian.com/bitbucket/files/304578655/755335794/2/1502737357377/add_ssh_key.png)

6. Click **Save**.

7. Check if it worked in terminal.
    * `ssh -T git@bitbucket.org`
    * You should see that your logged in as your username.

8. Now you can use the SSH URL next time you clone the repo.

## Branch Structure ##

We are using 2 main branches.

1. `master`
    * This is our production branch. Everthing that has been tested is put here for release.

2. `dev`
    * This is our development branch. All feature branches get merged here for testing.

## Git Workflow ##

1. Clone the repo.
    * `git clone git@bitbucket.org:cis422f19team4/project1.git`

2. Fetch the latest changes.
    * `git fetch`

3. Checkout the development branch
    * `git checkout dev`

4. Create a new branch for your feature
    * `git checkout -b feature-name dev`
    * This creates a new branch named `feature-name` based off of the `dev` branch. It automatically switches you to the new branch so you are now ready to work.

5. Make your changes.

6. Commit your changes.

7. Push your changes.
    * `git push -u origin feature-name`
    * This pushes your feature branch up to the repo on Bitbucket.

8. Open a pull request on Bitbucket.
