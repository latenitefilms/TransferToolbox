# Download

!!!success
Massive thanks to the **107 beta testers** on Apple's TestFlight for all their support and positive feedback!
!!!

---

You can download **Transfer Toolbox v1.0.2** for free [here](https://github.com/latenitefilms/TransferToolbox/releases/download/1.0.2/Transfer-Toolbox-1-0-2.zip).

---

!!!primary ☕️ Buy Us a Coffee!
If you find Transfer Toolbox useful, consider [buying us a coffee](https://www.buymeacoffee.com/latenitefilms){target="_blank"} or [sponsoring CommandPost](https://commandpost.io/sponsor/){target="_blank"}.
!!!

---

### Why it this now free?

Our original intention was to release this as a paid app on the Mac App Store for a one-time payment of **4.99** (in your local currency).

Frustratingly, Apple approved Transfer Toolbox v1.0.0 on **26th May 2023 at 08:57**, but then claimed "Developer Removed from Sale" at **10:06** (which we didn't).

With no way to undo this, we were forced to submit a new binary, v1.0.1.

This was accepted by TestFlight, however, it was rejected by App Review on **3rd June 2023 at 07:04**, due to:

> **Guideline 2.5.1 - Performance - Software Requirements**<br />
> We noticed your app allows users to import Final Cut Pro on Mac projects to Final Cut Pro on iPad, which is not a supported path at this time.<br />
><br />
> Final Cut Pro supports sharing projects from iPad to Mac. Due to differences in the file formats, attempting other unsupported and undocumented paths may lead to broken projects or other issues.

These guidelines are very specific:

> 2.5 Software Requirements<br />
> 2.5.1 Apps may only use public APIs and must run on the currently shipping OS. Learn more about public APIs. Keep your apps up-to-date and make sure you phase out any deprecated features, frameworks or technologies that will no longer be supported in future versions of an OS. Apps should use APIs and frameworks for their intended purposes and indicate that integration in their app description. For example, the HomeKit framework should provide home automation services; and HealthKit should be used for health and fitness purposes and integrate with the Health app.

As far as we can determine, Transfer Toolbox doesn't actually break this guideline.

We took advantage of the App Review Board, and their Unfair Treatment appeal option, however, it was determined that we're still breaking Guideline 2.5.1.

After a phone call with the App Review Board on **16th June 2023**, we then sent them this message, but have yet to hear back:

> Thank you for taking the time to discuss and clarify the issues surrounding our app, Transfer Toolbox. I appreciate your detailed feedback and the reasoning behind the decision to reject the app.
>
> While this outcome is indeed frustrating, I understand your concerns. However, I would like to delve a bit deeper into the reasoning. My understanding was that the Apple App Store operates independently of Apple's internal software divisions. The App Store is filled with apps that offer additional functionality to third-party applications, and indeed to Apple's own software products, all of which coexist without requiring explicit approval or consent from these third-party developers.
>
> Consider the utilities on the Mac App Store that modify files of third-party applications, or those that enable migration from legacy Apple products like Final Cut Pro 7 to Final Cut Pro X - a transition path not officially supported by Apple. I always believed that the App Store worked in harmony with commercial software products like Final Cut Pro and Logic Pro, rather than in conflict with them.
>
> The rejection of Transfer Toolbox appears to hinge on potential issues that Final Cut Pro for iPad users might encounter when importing libraries from the Mac version of the software. However, if such a situation arises, it would likely be an issue with Final Cut Pro for iPad rather than a fault of Transfer Toolbox. Our app is a simple tool that performs no more than what a user can manually do themselves. It merely moves a folder into another folder, using only public APIs and without any use of undocumented or private APIs.
>
> Moreover, we currently have 103 TestFlight users who are not only successfully using the app without issues but also derive immense value from it. This is a clear indication that our app caters to a demand and is loved by its users.
>
> Regarding Guideline 2.5.1 - "Software Requirements":
>
> 1. Use of Public APIs: Our application strictly adheres to Apple's design and programming standards, using only public APIs.
>
> 2. OS Compatibility: Transfer Toolbox is fully functional on the current OS, as evidenced by our TestFlight users.
>
> 3. Modern Technologies: The app is built using state-of-the-art technologies like Swift and SwiftUI, ensuring compatibility with future updates.
>
> 4. Absence of Deprecated Features: We have ensured that the application contains no deprecated features, frameworks, or technologies.
>
> 5. Proper Use of APIs and Frameworks: All APIs and frameworks in the application are used for their intended purposes, adhering to the guidelines.
>
> Therefore, it is unclear how Guideline 2.5.1 applies to the reason for rejection: "Your app allows users to import Final Cut Pro on Mac projects to Final Cut Pro on iPad, which is not a supported path at this time." I believe that the rejection of Transfer Toolbox is linked to Apple's desire to avoid potential bugs or additional support requests, not because it violates any specific guidelines.
>
> I would appreciate further clarification on how this guideline applies to our app and would suggest that the App Store Review Guidelines need a review if they implicitly include conditions related to the preferences of Apple's internal software teams. As a third-party developer, I understood that the App Store's primary purpose was to allow developers to extend the Apple ecosystem without the fear of being disadvantaged by Apple's internal software divisions.
>
> Many utilities on the Mac App Store perform actions that the original software developers did not intend or support - and that is what makes them valuable to users.
>
> While I respect and accept your decision, I believe it's important to consider the true nature and value of utilities like Transfer Toolbox. Therefore, I will proceed to release the app outside of the Mac App Store, albeit with disappointment and frustration.
>
> Thank you again for your time and consideration, and I look forward to your further clarification on this matter.

It seems unlikely that Apple will ever change their position, so we've decided to just release this for **free**, as we feel it's still a very useful feature for the Final Cut Pro community.

It's our expectation that **eventually** Apple will [Sherlock](https://512pixels.net/2013/12/the-brushed-metal-diaries-sherlock/){target="_blank"} Transfer Toolbox, and build in the native ability to get between Mac and iPad - hopefully via iCloud. However, given it's been over a decade and we still don't have a native scrolling timeline in Final Cut Pro for Mac, who knows when it'll happen.