# OpenChat GitHub Bot Action

A GitHub Action to post PR data to the OpenChat github bot.

## Inputs

- `OC_BOT_URL`: The URL of the bot endpoint. **Required**
- `OC_API_KEY`: The API key which encodes the group or channel to post the update to. **Required**

### Notes

The `OC_BOT_URL` should typically be set to `https://d3c0cjf1q5vuz2.cloudfront.net/pr_created`. This is provided as a variable in case the location changes in the future.

The `OC_API_KEY` should be set to the value of a group or channel level API key generated from the installed bot with OpenChat.

Our recommendation is to store both variables as secrets in your repository.

## Example Usage

```yaml
- uses: open-chat-labs/github-bot-action@v1
  with:
    OC_BOT_URL: ${{ secrets.OC_BOT_URL }}
    OC_API_KEY: ${{ secrets.OC_API_KEY }}
```
