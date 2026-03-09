# Public.com Perplexity Agent Skill

## Overview

This is an agent skill for interacting with your Public.com brokerage account via Perplexity Computer. You can get live quotes, place orders, get portfolio info, and more.

## Disclaimer

For illustrative and informational purposes only. Not investment advice or recommendations.

We recommend running this skill in as isolated of an environment as possible. If possible, test the integration on a new Public account as well.

## Before You Get Started

There are a few prerequisites needed to get started:

- To run in Perplexity Computer, you need a Perplexity Max subscription. You can sign up here: https://www.perplexity.ai/
- **Public.com account** — You'll need a Public brokerage account. Create one at https://public.com/signup if you don't have one.
- **Public.com API key** — Once you create your Public.com brokerage account, get an API key at https://public.com/settings/v2/api

## Configuration

This skill uses two environment variables. When you first use the skill you will be asked to enter these:

| Variable | Required | Description |
|---|---|---|
| `PUBLIC_COM_SECRET` | Yes | Your Public.com API secret key |
| `PUBLIC_COM_ACCOUNT_ID` | No | Default account ID for all requests |

## Adding Skill to Perplexity Computer

- Download this agent skill as a .zip from GitHub. It needs to be in a .zip file as that is the format Perplexity supports.
- Once you have the skill downloaded and your Perplexity account setup, navigate to https://www.perplexity.ai/computer/skills. This is where you will add the custom skill.
- At the top right click on `+ Create Skill -> Upload a skill`
- Attach the .zip file containing the skill
- Once the skill is added, create a `New Task` in Perplexity Computer and enter a prompt related to your Public account. For example `How is my Public portfolio doing today?`
- The prompt should load the skill into Perplexity Computer and you should be asked to enter your Public API key and default account number.
- From here on, so long as your Public API key stays valid you can ask questions related to your Public accounts.

## Example Prompts

- How is my portfolio doing today?
- Can you get me the options chain for Nvidia for options expiring around the next earnings?
- Can you get me the current quotes for Apple, Google, and Microsoft?
- Can you get my account history and list out and the deposits I've made?
- Set up a job to monitor the price of Bitcoin every 30 minutes. If the price is below $75K, buy $100 worth of it. If you are in a position and the price goes above $80K, sell it. All orders are market orders and only be in one position at a time. Run indefinitely.
- Get the options chain for Apple option contracts expiring Feb 18th. I want to open a call credit spread. Determine the best options contracts to do this with based on contract liquidity and max premium for cost.
