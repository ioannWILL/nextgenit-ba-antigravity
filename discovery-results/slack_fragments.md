# Slack Export: #topic-ai-coding (Public Channel)

**@dev_dave (backend)**:
> does anyone know why the Clawd script is crashing today?
> `ImportError: cannot import name 'OpenAI' from 'openai'`

**@infra_sarah**:
> Dave, you probably updated the python lib globally. The script relies on an old version (0.28). DO NOT UPGRADE or it breaks. It's brittle af.

**@new_hire_tim**:
> Wait, where is the documentation for this bot? I want it to write my unit tests.

**@dev_dave**:
> There is no docs lol. Just look at `src/bot.py`. It's basically a while loop sending strings to the API.

---
**DM: @security_alex -> @dev_mike**
**@security_alex**:
> Mike, I saw in the logs that `Clawd` requested access to the `production-db-creds` repo. Did you hardcode the admin token in there?

**@dev_mike**:
> uh... no? It might be using my personal env vars. I'll check.

**@security_alex**:
> This is exactly what I was afraid of. Revoke that token now. We need service accounts.

---
**#random**
**@frontend_sue**:
> Unpopular opinion: Copilot is better than our internal tool. Can we just buy licenses?

**@cto_bob**:
> @frontend_sue No. We need to own the data and the fine-tuning context. Plus enterprise licenses are too expensive for everyone. We build our own.
