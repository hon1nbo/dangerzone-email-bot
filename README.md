# dangerzone-email-bot
Email inbox automation for Dangerzone

## What is Dangerzone?
Dangerzone is an awesome tool for sanitizing untrusted documents. It's Free Open Source Software, and can be found in the [Dangerzone Github](https://github.com/freedomofpress/dangerzone).

#### Local Only
Dangerzone has a limitation in that it only runs on your local machine with the standard code base. This is by design because
1. It prevents a central server from having caches of documents that are subject to AHJs
2. It uses containers for the sanitization work, and these may not scale well on a multi-user instance

## What is the Dangerzone Email Bot?
The bot has a simple task: monitor an email inbox and when an attachment comes in sanitize it before returning it back to the user. This is intended for use within corporate or private networks, rather than a publicly accessible email inbox due to similar scaling issues as a web interface.

#### Why Email?
Making it an email bot allows forwarding a received email straight to Dangerzone, including from a mobile device that can't run it. Even for downloaded files it can simply be sent to the bot. A web interface is possible, but if you can avoid downloading the unsafe file then all the better.

## What about Privacy?
I'm working on making this a turnkey system that can be snapshotted without any sensitive data. The system would delete any copies of files after it has completed a task, and on the infrastructure level you could delete and reinstate the image as much as you want as long as the email environment variables for access are there.

## What's the current state?
Current state is "it's an idea with a little scripting currently in the works." Once I have a clean build it will be uploaded. Admittedly this is a side project for me and something that I've mulled for a while. I decided to take a fresh stab at it recently for various reasons.
