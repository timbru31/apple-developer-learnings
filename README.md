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

## Difference between the seller and developer name.

The are two types of names the end user will see in the App Store.  
1. The developer name
2. The seller name

**They can be different!**  

### Seller name
The *seller* name is the name of the legal entity that was registered as a developer. It's displayed in the detail page of the App Store as the *Developer* in the *Information* list. Confusing is that the seller name is displayed as the *developer* in the *Information* list. It used to be *Seller* in the past, accroding to screenshots.

### Developer name
The *developer* name can be customized **once**, when you initially create the app. It's displayed under the app name, right at the top in the search and the detail page.

#### More information

There is of course a Stack Overflow question with answer (here: https://stackoverflow.com/q/23738192/1902598) and the iTunes Connect Developer Guide has a page for *Identifying Your App in iTunes Connect* here: https://developer.apple.com/library/content/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Chapters/FirstSteps.html

## VPP requires a new Apple ID

You can't *upgrade* or *enable* an existing Apple ID for the VPP (Volume Purchase Program) in order to download purchased apps or receive custom B2B apps. It requires a new Apple ID. The best thing to do is: Let the VPP admin invite users. Then they create the correct type of Apple ID.

## iTunes Connect ❗️= Apple Developer membership

It's not enough to be part of the Apple Developer account. Being a member does not grant you access to iTunes Connect. **You need to be invited separately**, otherwise you receive the unobvious error message

> Your Apple ID isn't enabled for iTunes Connect. Learn More

after clicking the iTunes Connect button from the Developer Portal.

#### More information

The *Learn more* link does not work. Don't bother following it.  
Instead the solutuon is stated on Stack Overflow, as always: https://stackoverflow.com/q/28867975/1902598

## Signing with one account, uploading to another account

tbd

## VPP requires a "Paid Applications contract"

tbd

## You can't delete apps from iTunes Connect

tbd
