---
layout: archive
title: "How to use the service"
permalink: /how-to-use-service/
author_profile: false
---

## Getting Started
1. Access [telegrambot](https://telegram.me/sendrequest_bot), if you are on pc, please install [telegram desktop](https://desktop.telegram.org/) before using it.
If you are using mobile device, then please install telegram apps to talk to the bot.

2. Press start when you start talking to the bot.

3. You can check the command list of the bot by typing `/`, to demonstrate a normal process, we will start by using `/createjob` to create a new job. The id will be current time @GMT +0:00

4. With a new job, we can then upload contracts onto the service. Note that the service will only accept complied version of smart contract, the service will not compile it for you.

5. To upload an abi, you can just copy and paste the abi onto a file named `<yourcontract>.abi`, or alternatively you can upload a file name` <yourcontract>.json` generated from truffle.

6. To upload bytecode, please copy and paste the binary code (e.g.: 60806040.......) into a file named `<yourcontract>.bin`. Please make sure the filename of step 5 and 6 match with each other for a contract.

7. If filename match and the upload don't have problem, you should see a message of `Job is Ready to start`.

8. if you want to upload more contracts, repeat step 5-7, else use `/startjob`, choose the job you upload files to and choose the pricing option

9. If everything is all right, the job will be queued and will wait to start fuzzing, to know the status of the job, you can use `/inspectjob` to check it

10. When you see the job status is finished, you can get back the results using `/getresult`. To understand the result, please look at section <Test Report>.

Please note that once you start job, you cannot cancel the job or modify the contents inside the job.

## Commands that are helpful

* `/removefile` can be used when you have uploaded the wrong file, it can only be used when the job is not started.

* `/copyjob` can be used when you want to test some contracts again, you can modify the job by using `removefile` and upload file again.

* `/removejob` will remove everything of the job inside the server including the files you uploaded, results.
