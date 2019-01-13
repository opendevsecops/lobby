[![Follow on Twitter](https://img.shields.io/twitter/follow/opendevsecops.svg?logo=twitter)](https://twitter.com/opendevsecops)

# Ideas

We are full of ideas which are not yet implemented. **They are free to steal!** But if you want to make the world a better place you will use the OpenDevSecOps platform to make them real.

## Defensive Security

This is our bread and butter.

  * [ ] **CVE search** - define a list of technologies you want to monitor and get notifications (slack, email, sms, etc) when a possitive match is found. This will help you get notified of vulnerabilities as soon as they are made official.
  * [ ] **Temp shell** - a fully working remote shell with extra logging. This could be something like xterm.js over websockets. The idea is that the shell will be logging everything to stdout which will respectively get logged in cloudwatch, etc. Additional post processing rules can be used on the logs to do whatever heart desires.
  * [ ] **Access bot** - a bot that could give you a temp access to cloud resources when asked. Not a bullet proof security but at least it is transparent especially if used over a public channel on slack. At least everyone knows who does what.
  * [ ] **Secure drop** - companies share files with 3rd-party services with dubious T&Cs and crazy security. This solution is to provide an off-the-shelf dropbox-like solution for sharing files. We need a bucket, sftp, some static site for uploading and a well defined process for doing the encryption with keys not 7zip passowrds.

## Offensive Security

You cannot defense without understanding offensive.

  * [ ] **Pentest box** - it is what is sounds like. Additionally the box can be configured to be started at specific windows for specific purposes. For example, launching a pentesting infrastructure in your prod environment is not particularly great idea but perhaps the risk is mitigated if the box is only available for a limited period of time to complete a particular task.
  * [ ] **Automated scout** - does the recon and everything else under the sun to identify potential weaknesses. The solution can be run continiously to ensure all that is discloused online cannot be used in various attack scenarios.
  * [ ] **Cloud backdoors** - a collection of cloud backdoors. If we don't implement them how are we going to detect them? We cannot so don't judge.
  * [ ] **Phishing automator** - will help with running internal phishing exercises. Can it be used by to cause damage - of course? But we are not helping if we don't implement it. We will be ignoring the problem if nothing else.
  * [ ] **APT automator** - some tools can be dynamically setup to perform APTs. Metasploits comes to mind as the default solution but it could be anything really.
  * [ ] **Offensive Search** - an elastic search infrastructure for random indexes of data that can be used for offensive and perhaps defensive security. Imagine you are agregating a lot of interesting data but you don't know how to make sense of it. This could be the tool for the job.
