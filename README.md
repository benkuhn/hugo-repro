Steps to reproduce:

1. Install hugo 0.66
2. Run `echo $RANDOM; ( sleep 1 ; sed -i '' -E "s/Number:[0-9]+/Number:$RANDOM/" content/posts/drafts/a_draft.md ) & hugo server --buildDrafts`
3. Wait for the line `Source changed "/Users/ben/code/hugo-repro/content/posts/drafts/a_draft.md": CREATE` to appear
4. Navigate to `localhost:1313` and observe infinite loading
