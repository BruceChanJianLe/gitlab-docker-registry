# Gitlab Docker Registry

This repository demonstrates the usage of docker login with gitlab registry.  

## Creating Gitlab Personal Token

You can create as many personal access tokens as you like from your GitLab profile.  

1. Sign in to GitLab.
1. In the upper-right corner, click your avatar and select **Settings**.
1. On the **User Settings** menu, select **Access Tokens**.
1. Choose a name and optional expiry date for the token.
1. Choose the [desired scopes](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html#limiting-scopes-of-a-personal-access-token).
1. Click the **Create personal access token** button.
1. Save the personal access token somewhere safe. If you navigate away or refresh your page, and you did not save the token, you must create a new one

## Usage

Before you can build, pull and push images, you must authenticate with the Container Registry.  

```bash
# Example 1
docker login registry.example.com -u <username> -p <token>
# Example 2
docker login registry.gitlab.com/ghostrobotics/ghost_gazebo -u chanjl -p XXXXXXXXXXXXXXXXXXXX
```
Remember that -p is not password but instead the secret token that you have generated.  

## Reference

- Personal Access Tokens [link](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html)
- Usage [link](https://docs.gitlab.com/ee/user/packages/container_registry/)
