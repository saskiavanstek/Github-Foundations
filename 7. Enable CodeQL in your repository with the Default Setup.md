# Enable CodeQL in your repository with the Default Setup

1. On GitHub, navigate to the repository's main page
2. Under your repository name, select **Security**
3. Select **Set up code scanning**
>[!NOTE]
>If the option is not available, GitHub Advanced Security is not enabled.
4. In the **Set up** drop-down, select **Default**
5. Review the default options. If needed, select the **Edit** button in the bottom left corner of the new windows to customize how CodeQL runs.
>[!TIP]
>The ```on:pull_request``` and ```on:push``` triggers are the default for code scanning. They are useful for different purposes.
>You will learn more about these triggers in the upcomming modules
6. Select **Enable CodeQL** once you are ready to turn on code scanning
>[!TIP]
>In the default CodeQL analysis workflow, code scanning is configured to analyze your code each time you either push a change
>to any protected branches or raise a pull request against the default branch.
>Once the push is made, code scanning runs automatically.

