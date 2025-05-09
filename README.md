# OpenChat GitHub Webhook Action

A GitHub Action to post PR data to an OpenChat webhook.

## Inputs

- `OC_WEBHOOK_URL`: The webhook url to post to. **Required**

### Notes

You can obtain a webhook url by running the `/register_webhook` command within a group or channel that you own.

Our recommendation is to store url as a secret in your repository.

## Example Usage

```yaml
- uses: open-chat-labs/github_webhook_action@v1.0.7
  with:
    OC_WEBHOOK_URL: ${{ secrets.OC_WEBHOOK_URL }}
```
