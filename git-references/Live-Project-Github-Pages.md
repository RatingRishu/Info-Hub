# GitHub Setup and Initial Commit

# Configure Git with your username and email
git config --local user.name "YourUsername"
git config --local user.email "youremail@example.com"

# Check the status of your repository
git status

# Add all changes to the staging area
git add .

# Check the status again to confirm changes are staged
git status

# Rename the branch to main (if necessary)
git branch -M main

# Commit the changes with a message
git commit -m "first commit"

# Add the remote repository URL (replace with your repository URL)
git remote add origin https://github.com/YourUsername/YourRepository.git

# Push the changes to the remote repository on the main branch
git push -u origin main


# Making the Angular Project Live

# Install angular-cli-ghpages package
ng add angular-cli-ghpages

# Commit the changes after adding the package
git add .
git commit -m "Add angular-cli-ghpages package"

# Push the changes to the remote repository
git push

# Go to GitHub repository settings > Pages
# Update the source to 'main' branch and save

# Build the Angular project with the base URL (replace with your GitHub Pages URL)
ng build --base-href "https://YourUsername.github.io/YourRepository/"

# Deploy the project to GitHub Pages
npx angular-cli-ghpages --dir=dist/your-project

# Go to GitHub repository settings > Pages
# Update the source to 'gh-pages' branch and save

# Your repository page is now live
