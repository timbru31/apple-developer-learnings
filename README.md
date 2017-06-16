# The road to publish an app to the App Store 😣

This is a collection of loose things that I (we) learnt the hard way.  
Most of them are difficult to find, to understand and not obvious.

I hope to save some headache for other people who want to publish an app.

## Organization ❗️= Enterprise account

Apple differentiates three types of developer accounts for business (excluding education and MFi):

* Individuals
* Organizations
* Enterprise Program

The most important thing: **Enterprise accounts can not publish in the App Store**. They can only distribute via In-house App Distribution.  
This means *BYOD* (bring your own device) is impossible, if the customer should be able to download the app from the App Store.

#### More information

Apple has indeed a page that compares the different memberships. It's clearly stated, but not easy to find.
It's located here: https://developer.apple.com/support/compare-memberships/


## Debugging iOS applications

If you ever tried to debug the application on a real device, and not a simulator, I bet you've encountered the following error message:
> failed to get the task for process <xyz>

This error message simply means: don't use a distribution profile for debug signing.  
While this behavior is totally comprehensible, because the end-user shouldn't be able to debug your app, the error code is very misleading.

**The fix for this is: use a developer profile for debugging/signing.**

#### More information

If you google the error message, you end up visiting a page on Stack Overflow, where the answer has more than 630 upvotes. Maybe Apple can introduce a better error message in the future...  
You can find the question with the answer here: https://stackoverflow.com/q/11601304/1902598
