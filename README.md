# IITD proxy
Source: https://poorvi.cse.iitd.ac.in/~anupam

# Login Using Script
- Download the proxy script using the following command: `wget www.cse.iitd.ac.in/~anupam/proxy.sh`. You must be on IITD's intranet to access this file. 
- Edit the file to include your username/password. Also, if you're not a PhD student, you'll have to modify `proxy61` to the appropriate url in the script.
- Make the script executable using the command: chmod a+x ./proxy.sh
- Create a screen session.
  - Run the script using `./proxy.sh`. It should print "proxy login" if everything went correctly.
  - Leave the program running and detach the screen.
- On the terminal, set the variables:
  - `export http_proxy="http://proxy61.iitd.ac.in:3128"`
  - `export https_proxy="http://proxy61.iitd.ac.in:3128"`
  - If you are a sudo user, you can add them to your bashrc to avoid doing this every time you login.
- Check your internet connectivity using `wget www.google.com`. It should download an `index.html` file containing the `google.com` html and no errors.
- Note that if you're using sudo, use `sudo -E` to export the `http_proxy` and `https_proxy` variables. Then the internet would work for root as well.
