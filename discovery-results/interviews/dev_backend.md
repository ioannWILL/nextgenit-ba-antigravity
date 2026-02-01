# Interview Notes: Backend Engineer (Mike)
Date: 2025-10-12
Interviewer: [Previous BA]

## Topic: Current AI usage vs New Platform

**Q: How are you using the current 'Clawd' bot script?**
Mike: It's basically a python script wrapping the API. I run it locally. It helps with regex and boilerplate. But honestly, the shared API key situation is a nightmare. changing it every time someone leaves? annoying.

**Q: What's the biggest pain point?**
Mike: Rate limits. If the frontend team runs their integration tests, my local bot dies. We need per-user quotas or something. Also, it hallucinates libraries we don't use.

**Q: Needs for the new internal platform?**
Mike:
- It needs to run inside our VPC? Maybe? Or at least use our Artifactory proxy.
- I don't want a web UI. I want a CLI that actually works.
- It should integrate with Jira. I hate copying ticket descriptions into the prompt manually.

**Q: Concerns?**
Mike: Security team will kill it if it sends our code to the public model. Do we have a localized model? Or enterprise agreement?
Also, the current codebase in `src/bot.py` is spaghetti. hardcoded endpoints everywhere.

**Q: Anything else?**
Mike: Yeah, Sarah from data science has a fork of it that does SQL generation. whatever we build should probably support that too.
