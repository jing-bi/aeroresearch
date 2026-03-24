<h1 align="center">AeroResearch</h1>

<p align="center">
  <a href="https://mcp.jing.vision/aeroresearch">
    <img src="https://img.shields.io/badge/MCP-Remote-blue?style=flat-square" alt="MCP Remote" />
  </a>
  <a href="https://research.jing.vision">
    <img src="https://img.shields.io/badge/Auth-OAuth-success?style=flat-square" alt="OAuth" />
  </a>
  <a href="https://opencode.ai/docs/#install">
    <img src="https://img.shields.io/badge/Recommended-OpenCode-black?style=flat-square" alt="Recommended OpenCode" />
  </a>
  <a href="https://mcp.jing.vision/aeroresearch">
    <img src="https://img.shields.io/badge/Use%20Case-Research%20Exploration-blueviolet?style=flat-square" alt="Research Exploration" />
  </a>
  <a href="https://research.jing.vision">
    <img src="https://img.shields.io/badge/Release-Alpha-orange?style=flat-square" alt="Alpha Release" />
</a>
</p>

<p align="center">
  AeroResearch makes uncovering insights feel effortless.<br />
  Instead of heavy academic workflows, it provides agents with a clean way to <strong>explore</strong>, <strong>inspect</strong>, and <strong>export</strong> research.
</p>


## Account

AeroResearch is currently in **alpha**; OAuth signup is handled through a signup URL.

It uses the same account system as [research.jing.vision](https://research.jing.vision).

- If you already have an account, use it to sign in.
- If you don't have an account, DM me for the signup URL.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-jing--bi-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jing-bi)
[![X](https://img.shields.io/badge/X-@jingbix-black?style=flat-square&logo=x&logoColor=white)](https://x.com/jingbix)


## Example Use Cases

<p align="center">
  <sub>Assume <code>@paper-list.md</code> contains the following papers:</sub>
</p>

```md
- https://arxiv.org/abs/2511.15613
- https://arxiv.org/abs/2412.18108
```

<details open>
<summary><strong>📚 Can you read <code>@paper-list.md</code> and generate a <code>cite.bib</code> for all referenced papers?</strong></summary>

<br>

```bibtex
@article{bi2025whentothink,
  title   = {When to Think and When to Look: Uncertainty-Guided Lookback},
  author  = {Bi, Jing and Bellos, Filippos and Guo, Junjia and Li, Yayuan and Huang, Chao and Tang, Yolo Y. and Song, Luchuan and Liang, Susan and Zhang, Zhongfei Mark and Corso, Jason J. and Xu, Chenliang},
  journal = {arXiv preprint arXiv:2511.15613},
  year    = {2025}
}

@inproceedings{bi2025unveiling,
  title     = {Unveiling Visual Perception in Language Models: An Attention Head Analysis Approach},
  author    = {Bi, Jing and Guo, Junjia and Tang, Yunlong and Wen, Lianggong Bruce and Liu, Zhang and Xu, Chenliang},
  booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
  year      = {2025}
}
```

</details>

<details>
<summary><strong>📊 What datasets are used in the papers listed in <code>@paper-list.md</code>? Give me a table.</strong></summary>

<br>

| Paper                                              | Main datasets / benchmarks                                  |
| -------------------------------------------------- | ----------------------------------------------------------- |
| **When to Think and When to Look**                 | MMMU-val, MMBench, MMStar, MathVista, MathVision, MathVerse |
| **Unveiling Visual Perception in Language Models** | PointQA, MMBench, POPE, SEED, QBench, Visual General        |

</details>

<details>
<summary><strong>🧠 Read the papers in <code>@paper-list.md</code> and compare what each one is actually for.</strong></summary>

<br>

| Paper                                              | What it does                                                                                            | Best use                                                                      |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| **When to Think and When to Look**                 | Studies when test-time thinking helps LVLMs, then adds an uncertainty-guided lookback decoding strategy | Evaluating or improving visual reasoning at inference time                    |
| **Unveiling Visual Perception in Language Models** | Analyzes attention heads to identify how language models process visual tokens                          | Interpreting multimodal models and understanding visual perception mechanisms |

</details>

<details>
<summary><strong>📝 From <code>@paper-list.md</code>, give me a concise research brief I can paste into notes.</strong></summary>

<br>

* **When to Think and When to Look** — shows that more reasoning is not always better for LVLMs, and proposes uncertainty-guided lookback to improve grounding and benchmark performance.
* **Unveiling Visual Perception in Language Models** — shows that certain attention heads specialize in visual content, helping explain how language models adapt to multimodal inputs.

</details>



## How to Use
### OpenCode
OpenCode is the easiest and most beginner-friendly way to get started.  
It is free to use with the `opencode/minimax-m2.5-free` model.
#### Option 1: Interactive Setup (Recommended)


Install OpenCode using the official [installation guide](https://opencode.ai/docs/#install), then add the remote MCP server with the `opencode mcp add` command:

```text
┌  Add MCP server
│
◇  Location
│  Global (or Current Project, depending on your preference)
│
◇  Enter MCP server name
│  aeroresearch
│
◇  Select MCP server type
│  Remote
│
◇  Enter MCP server URL
│  https://mcp.jing.vision/aeroresearch
│
◇  Does this server require OAuth authentication?
│  Yes
│
◇  Do you have a pre-registered client ID?
│  No
│
◆  MCP server "aeroresearch" added to /Users/jing/.config/opencode/opencode.json
│
└  MCP server added successfully
```

Then run the following:

```bash
opencode mcp auth aeroresearch
```

This opens a browser window to authenticate with the MCP server.

#### Option 2: Manual Setup

You can also copy the `mcp` section from the example `opencode.json` below into your OpenCode config file (usually located at `~/.config/opencode/opencode.json`). Then authenticate using `opencode mcp auth aeroresearch`.

```json
{
  "$schema": "https://opencode.ai/config.json",
  "mcp": {
    "aeroresearch": {
      "type": "remote",
      "url": "https://mcp.jing.vision/aeroresearch"
    }
  },
  "model": "opencode/minimax-m2.5-free"
}
```

### Other Agents

#### Claude Code

Add the remote MCP server:

```bash
claude mcp add --transport http aeroresearch https://mcp.jing.vision/aeroresearch
```

Then open Claude Code and run the following:

```text
/mcp
```

Select the `aeroresearch` server and complete the OAuth flow in your browser.

#### Codex

Add the remote MCP server:

```bash
codex mcp add aeroresearch --url https://mcp.jing.vision/aeroresearch
```

Then authenticate using the following command:

```bash
codex mcp login aeroresearch
```

This opens the OAuth login flow in your browser.

#### Gemini CLI

Add the remote MCP server:

```bash
gemini mcp add --transport http aeroresearch https://mcp.jing.vision/aeroresearch
```

Then authenticate from inside the Gemini CLI by running:

```text
/mcp auth aeroresearch
```

This opens the browser-based OAuth flow.



