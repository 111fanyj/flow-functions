# WasmHaiku Flow Functions

![badge](https://github.com/second-state/flow-functions/workflows/build/badge.svg?style=flat-square)

## Usage

| Package Name | Inbound | Outbound | Description |
|------------- | ------- | -------- | ----------- |
| [getting-started](github/slack/getting-started/) | GitHub | Slack | Send a message to Slack when new comments are added to GitHub issues |
| [branch-tag-created](github/slack/branch-tag-created/) | GitHub | Slack | Send a message to Slack when a Git branch or tag is created |
| [branch-tag-deleted](github/slack/branch-tag-deleted/) | GitHub | Slack | Send a message to Slack when a Git branch or tag is deleted |
| [commit-syncer](github/slack/commit-syncer/) | GitHub | Slack | Send a message to Slack when a GitHub commit is pushed |
| [commit-comment-notifier](github/slack/commit-comment-notifier/) | GitHub | Slack | Send a message to Slack when a commit comment is created |
| [discussion-notifier](github/slack/discussion-notifier/) | GitHub | Slack | Send a message to Slack when a discussion is created, edited, deleted, pinned, unpinned, locked, unlocked, transferred, category_changed, answered, unanswered, labeled, or unlabeled |
| [discussion-comment-notifier](github/slack/discussion-comment-notifier/) | GitHub | Slack | Send a message to Slack when a comment in a dicussion is created, edited, or deleted |
| [fork-notifier](github/slack/fork-notifier/) | GitHub | Slack | Send a message to Slack when a user forks a repository |
| [issue-notifier](github/slack/issue-notifier/) | GitHub | Slack | Send a message to Slack when a GitHub issue is opened, edited, or assigned |
| [label-notifier](github/slack/label-notifier/) | GitHub | Slack | Send a message to Slack when a label is created, edited, or deleted |
| [pr-messager](github/slack/pr-messager/) | GitHub | Slack | Send a message to Slack when an activity related to a pull request was performed. Can be one of: assigned, auto_merge_disabled, auto_merge_enabled, closed, converted_to_draft, edited, labeled, locked, opened, ready_for_review, reopened, review_request_removed, review_requested, synchronize,unassigned, unlabeled, unlocked |
| [pr-review-notifier](github/slack/pr-review-notifier/) | GitHub | Slack | Send a message to Slack when a pull request review is submitted, edited, or dismissed |
| [pr-review-comment-notifier](github/slack/pr-review-comment-notifier/) | GitHub | Slack | Send a message to Slack when a  pull request review comment is created, edited, or deleted |
| [release-notifier](github/slack/release-notifier/) | GitHub | Slack | Send a message to Slack when a release is published, unpublished, created, edited, deleted, prereleased, or released |
| [repository-notifier](github/slack/repository-notifier/) | GitHub | Slack | Send a message to Slack when a repository is created, deleted, archived, unarchived, edited, renamed, transferred, publicized, or privatized |
| [star-messager](github/slack/star-messager/) | GitHub | Slack | Send a message to Slack when the GitHub repo gets every 10 stars |
| [workflow-job-notifier](github/slack/workflow-job-notifier/) | GitHub | Slack | Send a message to Slack when a GitHub Actions workflow job has been queued, is in progress, or has been completed |
| [star-thanks-by-gmail](github/gmail/star-thanks-by-gmail/) | GitHub | Gmail | Send thank you message via Gmail when GitHub repo gets star |
| [star-thanks-by-sendgrid](github/sendgrid/star-thanks-by-sendgrid/) | GitHub | Sendgrid | Send thank you message via Sendgrid when GitHub repo gets star |
| [label-issue-discord](github/discord/issue-to-discord/) | GitHub | Discord | Send a message to Discord when  with a label |
| star-messenger | GitHub | [Twilio](github/twilio/star-messenger/) / [Slack](github/slack/star-messager/) | Send thank you message via Twilio(or Slack) when GitHub repo gets star |
| [calculator](slack/slack/calculator/) | Slack | Slcak | Compute the expressions on the Slack |
| [lucky-draw](slack/slack/lucky-draw/) | Slack | Slcak | Simply type "lucky draw" in a Slack channel to do the trick |
| [assign-notifier](github/notion/assign-notifier/) | GitHub | Notion | Create a task on Notion when the GitHub issue is assigned |
| upload | Slack | [Cloudinary](slack/cloudinary/upload/) / [Dropbox](slack/dropbox/upload/) | Upload a file from Slack to Cloudinary(or Dropbox) |
| [image-rotator](cloudinary/slack/image-rotator/) | Cloudinary | Slack | Returns the URL of the image rotated by 90 degrees when a file is uploaded to the Cloudinary |

## Build for Rust functions

* Install WASM target if you not

  ```shell
  rustup target add wasm32-wasi
  ```

* Build packeage

  ```shell
  cargo build -p <package-name> --target wasm32-wasi --release # Build specified package
  cargo build --workspace --target wasm32-wasi --release       # Build all packages
  ```
