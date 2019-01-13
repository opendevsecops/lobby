[![Follow on Twitter](https://img.shields.io/twitter/follow/opendevsecops.svg?logo=twitter)](https://twitter.com/opendevsecops)

# Ideas

We are full of ideas which are not yet implemented. **They are free to steal!** But if you want to make the world a better place you will use the OpenDevSecOps platform to make them real.

## Defensive Security

This is our bread and butter.

  * [ ] **CVE search** - define a list of technologies you want to monitor and get notifications (slack, email, sms, etc) when a possitive match is found. This will help you get notified of vulnerabilities as soon as they are made official.
  * [ ] **Temp shell** - a fully working remote shell with extra logging. This could be something like xterm.js over websockets. The idea is that the shell will be logging everything to stdout which will respectively get logged in cloudwatch, etc. Additional post processing rules can be used on the logs to do whatever heart desires.
  * [ ] **Access bot** - a bot that could give you a temp access to cloud resources when asked. Not a bullet proof security but at least it is transparent especially if used over a public channel on slack. At least everyone knows who does what.
  * [ ] **Secure drop** - companies share files with 3rd-party services with dubious T&Cs and crazy security. This solution is to provide an off-the-shelf dropbox-like solution for sharing files. We need a bucket, sftp, some static site for uploading and a well defined process for doing the encryption with keys not 7zip passowrds.
  * [ ] **Config snapshot** - a tool plus some support infrastructure to make periodic config snapshots of the entire cloud setup. AWS Config does that already but do we trust it? People know ways to evadate it! This tool can be based on the NCC's ScoutSuite. The snapshot can be taken and compared with previous snapshots to detect changes.
  * [ ] **AWS Forensics** - an infrastructure to support forensic analysis in AWS. I don't know fully what this will look like but it sounds like something we need. Tranditional forensics simply does not work well enough in cloud. The project could define common use-cases and provide specific solutions for them.
  * [ ] **Security News Bot** - why manually keep everyone informed on slack and other channels when you can automate the process. A bot will keep you informed about what is going on 24/7. The bot can also come with configurable set of rules and filters. Perhaps we can deploy it in the OpenDevSecOps channel first.
  * [ ] **Bad Actors** - consume the public feeds from Firehol and produce files in s3. Use the files to feed into GuardDuty and other tools in order to quickly identify bad actors. I know, GuardDuty alegedly does something like this but can we trust it?
  * [ ] **Fake Profile Detector** - automate the process of finding fake profiles (LinkedIn) claiming to be the company or that work for the company. LinkedIn does not provide this automatically.
  * [ ] **Dependency Catalog** - create a depenency and artifacts catalog to identify vulnerabilities. Performing security checks at build time is cool but if you don't build frequently you will get nothing. This tool/infrastructure is designed to solve this problem by build a catalog of all dependencies and constantly check them for vulnerabilities.
  * [ ] **Autom subscription to HIBP** - create a fully automated solution for subscribing to HIBP and instantiating handlers to report when accounts are found in password leaks.
  * [ ] **Malicious domain detector** - anyone can register a domain name that looks like yours so how do you find them? Well this tool/infrastructure will help you do just that.
  * [ ] **Rota** - some people need access to things when they are on rota. This module is supposed to automate this process. Add the desired people to the rota and set their permissions. The tool will do the rest.
  * [ ] **Basic SOC** - people spend millions for SOC that does nothing and this is about to change. This module is envisioned to provide solutions to this age old problem.
  * [ ] **Log grep** - a serverless infrastructure for grepping the logs. Sometimes you just need to find keywords to create pretty simple but clever adhoc solutions.
  * [ ] **Country/Office lock** - sometimes you need to lock down access to your AWS to specific country/office. This module is supposed to help you set this up.
  * [ ] **Suspicious alarms** - monitor networks for trafic spikes. Setup alarms to help you flag this automatically.
  * [ ] **Killer** - the best type of infrastructure is the one that defends itself. This module will provide features to kill various types of resources such as EC2 instances, Lambda functions, etc. The idea is that you can invoke the killer if you think that the detect event is highlighy suspicious. This could cause some down-time if not configured properly but if properly configured will make your environment super hostile to attack.
  * [ ] **camouflage** - a lambda edge function to hide the reall application form non-standard user-agents. This will make pentesting so much difficult. We can even detect when sombody is doing something crazy and actively throw them at time-wasting resources.
  * [ ] **Sandbox** - a module to help you setup a proper sandbox environment that gets nuked on scheduled interval. You can use this to test cloud components at minimal cost.
  * [ ] **Bucketeer** - module to help you reserve common s3 buckets and other named resources. Some attackers will park your domains so we need this infrastructure to help mitigate against this.

## Offensive Security

You cannot defense without understanding offensive.

  * [ ] **Pentest box** - it is what is sounds like. Additionally the box can be configured to be started at specific windows for specific purposes. For example, launching a pentesting infrastructure in your prod environment is not particularly great idea but perhaps the risk is mitigated if the box is only available for a limited period of time to complete a particular task.
  * [ ] **Automated scout** - does the recon and everything else under the sun to identify potential weaknesses. The solution can be run continiously to ensure all that is discloused online cannot be used in various attack scenarios.
  * [ ] **Cloud backdoors** - a collection of cloud backdoors. If we don't implement them how are we going to detect them? We cannot so don't judge.
  * [ ] **Phishing automator** - will help with running internal phishing exercises. Can it be used by to cause damage - of course? But we are not helping if we don't implement it. We will be ignoring the problem if nothing else.
  * [ ] **APT automator** - some tools can be dynamically setup to perform APTs. Metasploits comes to mind as the default solution but it could be anything really.
  * [ ] **Offensive Search** - an elastic search infrastructure for random indexes of data that can be used for offensive and perhaps defensive security. Imagine you are agregating a lot of interesting data but you don't know how to make sense of it. This could be the tool for the job.
  * [ ] **VPN/SSH/Proxy Hopper** - simple container infrastructure to hop into a VPC remotely. This can be used to gain direct access to a well guarded network.
