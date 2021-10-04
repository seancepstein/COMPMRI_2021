# Setting up source control in Matlab

* [Install Matlab](https://uk.mathworks.com/academia/tah-portal/university-college-london-649021.html) using your UCL credentials.

* [Install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) (note: if you'rte running macOS/linux, git will be already installed and you can skip this step)

* [Generate ssh keys](https://uk.mathworks.com/help/matlab/matlab_prog/set-up-git-source-control.html) in OLD RSA FORMAT
    1. Follow the instructions in the above link, but replace `ssh-keygen` command with `ssh-keygen -t rsa -b 4096 -m PEM` to generate an SSH key in the old RSA format
    2. Do not set a passphrase when prompted

* Once you have placed your ssh keys in the appropriate folder (see link above), open the key (`id_rsa.pub`) in a text editor (do not make changes to it)

* Restart Matlab

* Create an account on [github](https://github.com) and [register for the student developer pack](https://education.github.com/pack)

* Go to github account settings -> `SSH and GPG keys` and click `New SSH key`

* Copy the contents of your ssh key (`id_rsa.pub`, previously opened in a text editor) and paste it into github. Give the key an appropriate name (e.g. `Sean's laptop`) and save

* Return to your main github page and create a new repository, giving it an appropriate name (e.g. `COMPMRI_2021`), setting it to `Private`, and creating a  blank `README.md`

* Open the newly created repository on github, and click the `Code` button in the top right. Select `SSH` and copy the link (e.g. `git@github.com:seancepstein/COMPMRI_2021.git`)

* In Matlab, right click on the `Current folder` panel (on the left) and select `Source control` -> `Manage files`

* Ensure `Source control integration` is set to `Git` and copy your previously-copied git link (e.g. `git@github.com:seancepstein/COMPMRI_2021.git`) into the `Repository path` box. Select an empty local path (where the repository will live locally on your computer) under `Sandbox`. Click `Retrieve`

* Right click on `README.md` and select `Source control` -> `Pull` to verify that authentication is working

* Go to your repository on github, select `Settings` -> `Manage access` -> `Add people` and add `garyhuizhang` and `seancepstein` as collaborators

All done!
