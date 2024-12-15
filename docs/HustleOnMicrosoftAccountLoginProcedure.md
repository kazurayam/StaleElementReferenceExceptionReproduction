# Microsoft Azure DevOps log-in process --- a dangerous zone

There are many posts in the Katalon user forum where people experienced SERE while they tried to automate the login process of Microsoft Azure DevOps.

<figure>
<img src="https://kazurayam.github.io/StaleElementReferenceExceptionReproduction/images/MS_Azure_sign_in_page.png" alt="MS Azure sign in page" />
</figure>

I tried to "fix SERE" at the MS Azure login page, but I failed. See [my previous post](https://forum.katalon.com/t/stale-element-not-found-is-this-relate-to-using-same-object/97973/103).

The log-in pages of Microsoft Azure are highly JavaScript-driven. I would warn you, it’s terribly difficult to automate. You would get SERE there due to the way how the target page is implemented. Don’t blame Katalon Studio for the difficulty.

# Other tools?

The StaleElementReferenceException keeps up with any Selenium WebDriver-based browser-automation tools including Katlaon Studio. On the other hand, there are new browser-automation tools based on the CDP/BiDi technology. For example, [Playwright](https://playwright.dev/). I guess that those new comers work better for the Azure DevOps log-in process. I hope someone to try it and report their experiences back here.

Refer to
<https://www.eliostruyf.com/automating-microsoft-365-login-mfa-playwright-tests/>