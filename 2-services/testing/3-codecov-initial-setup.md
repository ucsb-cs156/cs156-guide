# Codecov Initial Setup

Before Codecov can be used within the organization, we must first grant permission to access the organization's repositories and members. This only needs to be done once per organization and can be done by any organization owner, regardless of GitHub student status.

### If you have logged into Codecov with GitHub before:

1. Visit the [GitHub homepage](https://github.com/) and sign in to an owner's GitHub account.
2. When signed in, navigate to the [Codecov OAuth Application page](https://github.com/settings/connections/applications/c68c81cbfd179a50784a). This page will only appear if you've previously used GitHub to sign in to Codecov.
    * The page should look like this:

        ![Codecov OAuth Application page](../../images/services/testing/codecov-oauth-app-page.PNG)

3. Under "Organization access", find your class GitHub organization and click "Grant". Enter your password if prompted.
    
    ![Codecov Grant Button](../../images/services/heroku/heroku-grant-button.PNG)

    * If the organization has a green check instead of a red "X", an owner has already granted access and Codecov already has permissions to access your organization's repos and members, so nothing needs to be done.
    * If the button shows "Request" instead of "Grant", then you don't have owner permissions to the organization. You can click "Request", which will forward the request to all owners, one of which can approve the request. 

### If you have not logged into Codecov with GitHub before

1. Visit the [GitHub homepage](https://github.com/) and sign in to an owner's GitHub account.
2. Visit [Codecov](https://app.codecov.io/login/gh) and select "Login with GitHub".
    * By default, this should log you in with both the Public and Private repo scopes. If you are given an option to select, be sure to allow private repository access.
3. Under "Organization access", find your class GitHub organization and click "Grant". Enter your password if prompted.
    
    ![Codecov Grant Button](../../images/services/heroku/heroku-grant-button.PNG)

    * If the organization has a green check instead of a red "X", an owner has already granted access and Codecov already has permissions to access your organization's repos and members, so nothing needs to be done.
    * If the button shows "Request" instead of "Grant", then you don't have owner permissions to the organization. You can click "Request", which will forward the request to all owners, one of which can approve the request. 

4. Click the green button to "Authorize Codecov".
5. You should be taken to a list of repositories in Codecov. On the top left, verify that your organization is present when "All my orgs and repos" is clicked.

    ![Codecov Orgs List](../../images/services/testing/codecov-org-list.PNG)

## Verifying GitHub Students

In order for students to not occupy a seat in a Codecov organization, they must be verified as a student through [GitHub Education](https://education.github.com/pack), and Codecov must reflect this status in the organization member list.

To obtain student status in Codecov:

1. Sign up and get approved for GitHub Education.
    * This process should only take a few minutes if students have a verified UCSB email on their account.
    * Students can upload a picture of their student ID for verification, even if it does not show a date.
2. After getting approved, **sign into Codecov at least once**
    * Student statuses are only updated at login. If a student is already logged in from a previous session, they must sign out and sign back in.

