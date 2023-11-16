## What is a compiler?
A compiler takes code files and turns them into executable programs, we will cover the specifics of compilers later in advanced stuff

## Setup
Thanks to wsl, installing a compiler is a BREEZE, assuming you followed the setup, its as simple as opening a wsl terminal and running
```
sudo apt install clang
```
now lets break this command down
- Sudo, this basically says "run this as administrator" since we are installing a program it is needed, DO NOT RUN EVERY COMMAND WITH THIS
- apt, apt is the program we are running, it is Ubuntu's package manager, you dont really need to know what that means
- install, this tells apt that we are installing a specific package (*who would have guessed*)
- clang, this is the name of the program, most people pronounce it CLANG like the noise, but it stands for c language (im pretty sure)
The command will ask for your password so it can run as admin and then 