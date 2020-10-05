---
type: rule
title: Do you know to connect to VSTS Git with Personal Access Tokens
uri: do-you-know-to-connect-to-vsts-git-with-personal-access-tokens
created: 2017-07-03T05:46:30.0000000Z
authors:
- id: 24
  title: Adam Stephensen
- id: 58
  title: Jernej Kavka

---

​​​​When you create a new git repository and need to push it to VSTS you need to provide login credentials.​

It isn't always clear how to do this.
 
[[badExample]]
| ![ Bad Example - Alternate  Authentication Credentials should not be used. When you change the password it invalidates all projects and can't be scoped to limit access to your Team Services data](vsts-alternative-login.png)

Instead, you should use Personal Access Token. You can do this in two ways.

The first option is to make sure your Git for Windows is up-to-date and when cloning the repository, you use Microsoft Account to log in. Personal Access Token for Git will be created for you.

[[goodExample]]
| ![ Good Example - Windows for Git credential manager will automatically create Personal Access Token for Git](git-credentials-personal-access-token.png)

Option 2 is to manually create Personal Access Token and use it as a password for Git login.

You can follow this blog post for full instructions: [Using Personal Access Tokens to access Visual Studio Online](https://roadtoalm.com/2015/07/22/using-personal-access-tokens-to-access-visual-studio-online/).

[[goodExample]]
| ![ Good Example - You can also manually enter Personal Access Token into password section if the credential manager doesn't work​](git-credentials-personal-access-token-manual.png)
