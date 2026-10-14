# Mnestiq

**Forensic evidence for AI agents.**

When an AI agent does something it shouldn't, like emailing the wrong person or following
instructions hidden in a web page, someone has to work out what happened. Mnestiq records what
your agents saw, decided and did as signed, tamper-evident evidence. You can name the run, the
step, the input that drove it and who approved it, and prove the record wasn't changed afterwards.

## The recorder

[mnestiq](https://github.com/mnestiq/mnestiq) is the open evidence format, recorder, verifier and
local dashboard. Free and open source under Apache-2.0, so you can check exactly how your evidence
is made.

- Records model calls, tool calls and approvals, with where each piece of the model's input came
  from: the user, a web page, a tool, a document or another agent
- Hash-chained and signed, so any edit, deletion or reordering fails verification
- Signing keys kept outside the agent, in Azure Key Vault or a signing service, with independent
  RFC 3161 timestamps
- Works with Anthropic, OpenAI, Azure OpenAI and OpenAI-compatible models
- Fails open: if recording fails, the agent keeps running
- Runs on your own machines

```bash
pip install mnestiq
```

## Mnestiq Workbench

For security teams investigating agent incidents: alerts in Microsoft Sentinel, the agent's
evidence checked against network and cloud logs, and signed reports. In early access, see
[mnestiq.com/workbench](https://mnestiq.com/workbench).

## Get in touch

[Website](https://mnestiq.com) · [PyPI](https://pypi.org/project/mnestiq/) ·
[alexander@mnestiq.com](mailto:alexander@mnestiq.com) · Security issues through
[private vulnerability reporting](https://github.com/mnestiq/mnestiq/security)
