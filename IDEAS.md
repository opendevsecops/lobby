[![Follow on Twitter](https://img.shields.io/twitter/follow/opendevsecops.svg?logo=twitter)](https://twitter.com/opendevsecops)

# Ideas

We are full of ideas which are not yet implemented. **They are free to steal!** But if you want to make the world a better place you will use the OpenDevSecOps platform to make them real.

## Defensive Security

This is our bread and butter.

  * [ ] CVE search - define a list of technologies you want to monitor and get notifications (slack, email, sms, etc) when a possitive match is found. This will help you get notified of vulnerabilities as soon as they are made official.
  * [ ] Temp shell - a fully working remote shell with extra logging. This could be something like xterm.js over websockets. The idea is that the shell will be logging everything to stdout which will respectively get logged in cloudwatch, etc. Additional post processing rules can be used on the logs to do whatever heart desires.

## Offensive Security

You cannot defense without understanding offensive.

  * [ ] Pentest box - it is what is sounds like. Additionally the box can be configured to be started at specific windows for specific purposes. For example, launching a pentesting infrastructure in your prod environment is not particularly great idea but perhaps the risk is mitigated if the box is only available for a limited period of time to complete a particular task.
  * [ ] Automated scout - does the recon and everything else under the sun to identify potential weaknesses. The solution can be run continiously to ensure all that is discloused online cannot be used in various attack scenarios.
