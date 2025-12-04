# Install Node.js and npm

# Step 1: Use curl to download and set up Node.js 14.x from NodeSource PPA (Personal Package Archive)
# -sL: Silent mode, show progress; -o: Output to file
# This command automatically configures the apt package manager to get the latest version of Node.js 14.x
curl -sL https://deb.nodesource.com/setup_14.x | sudo bash -

# Step 2: Install Node.js
# -y: Automatically confirm all prompts, proceed with the installation
# This step installs Node.js and its dependencies
sudo apt -y install nodejs

# Step 3: Update npm to a specific version 9.6.5
# -g: Install npm globally, making it available system-wide
# This ensures you are using the specified version of npm
sudo npm install -g npm@9.6.5

# Verify the installation
# Check the Node.js version
node -v  # Should output v14.21.3

# Check the npm version
npm -v   # Should output 9.6.5
