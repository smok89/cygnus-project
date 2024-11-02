# Cygnus Project

This repository organizes three sub-repositories (`cygnus-core`, `cygnus-app-backend`, and `cygnus-app-frontend`) to manage the Rust microservice, Go backend, and Angular frontend for the Cygnus application.

## Project Structure

- **cygnus-core**: Rust-based microservice responsible for core blockchain operations.
- **cygnus-app-backend**: Backend in Go, acting as a middleware relay between the frontend and the Rust microservice.
- **cygnus-app-frontend**: Angular frontend application providing user interface for interacting with the blockchain.

## Cloning the Repository with Submodules

To clone this repository along with its submodules, use:

```bash
git clone --recurse-submodules git@github.com:username/cygnus-project.git
```

If you’ve already cloned the main repository without submodules, initialize and update them with:

```bash
git submodule init
git submodule update
```

## Working with Submodules

Each submodule is an independent Git repository, so you can navigate into each one to make changes, commit, and push as needed.

### Navigate to a submodule:

```bash
cd cygnus-core  # or cygnus-app-backend, or cygnus-app-frontend
```

### Make changes and commit within the submodule:

```bash
git add .
git commit -m "Your commit message"
```

### Push changes to the submodule’s remote repository:

```bash
git push origin main
```

## Updating Submodules

To fetch the latest changes made in the submodules from their remote repositories, run the following command in the root of the main project:

```bash
git submodule update --remote
```

## Updating the Main Repository after Submodule Changes

When you commit and push in a submodule, the main repository should also be updated to point to the latest submodule commit.

- Go back to the root of the main repository:

    ```bash
    cd ..
    ```

- Add and commit the updated submodule reference:

    ```bash
    git add cygnus-core  # or cygnus-app-backend, or cygnus-app-frontend
    git commit -m "Update submodule cygnus to latest commit"
    ```

- Push the commit in the main repository:

    ```bash
    git push origin main
    ```