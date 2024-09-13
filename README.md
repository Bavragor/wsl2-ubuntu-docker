# Install WSL2

Open the `windows terminal`

Check version with `wsl --version`, should be sth. like WSL-Version: 2.2.\*.\*

List all available distributions with `wsl --list --online`

Install latest LTS of Ubuntu with version from cmd before e.g. `wsl --install Ubuntu-24.04`

Create a `.wslconfig` in your home directory and add the following:
```
[experimental]
autoMemoryReclaim=gradual
```

Restart `terminal` and open ubuntu console, execute these:
```
sudo apt update
sudo apt upgrade
```

# Install Docker Desktop

Download and install the latest [docker desktop](https://www.docker.com/products/docker-desktop/) version.

# IDE Optimizations
```
sudo apt install inotify-tools
sudo sh -c "echo \"fs.inotify.max_user_watches = 524288\" >> /etc/sysctl.conf"
sudo sysctl -p
```