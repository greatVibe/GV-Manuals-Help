# Use The Main Row And Prompt Controls

The plus button to the left of the prompt reveals the main action row. This is
useful when you want to prepare context or open a workspace before sending a
prompt.

## Main Row Order

The cards appear in this order:

1. **Attach** — add images or files. Hold for camera, gallery, file, and paste
   choices.
2. **Sealed Secret** — seal a value for safe use. Hold for advanced secret
   options.
3. **History** — reuse earlier prompts. Hold for saved Scripts.
4. **Files** — browse files on the selected node. Hold for full-screen Files.
5. **IDE** — open the IDE workspace. Hold for gvAPI.
6. **ChitChat** — open live mesh messaging.
7. **Settings** — open settings for the selected node. Hold for full Settings.

Click the plus button again to hide the row. An agent can also reveal the row
and point at one or several cards without opening their destinations.

## Attach An Image

Image attachment uses the plus button, not a paperclip:

1. Click the **+** button beside the prompt.
2. Choose **Attach** from the main action row.
3. Choose **Gallery** to select an image from the device, or **Paste** when the
   image is already in the computer or mobile clipboard.

Camera and File remain available in the same Attach choices when those routes
fit better. A paperclip may appear on gvturns or other API results to attach
that item as prompt context; it is not the image-input control.

Ask **“Show me how to attach an image.”** The agent should present the ordered
`image-attachment-tour` guidance group from the dashboard element reference as
one smooth tour.

## Prompt Controls

The center text area is the prompt input. Your prompt goes to the node and AI
profile shown in the status bar.

Inside the right side of the text area, the composer button opens the full
prompt composer for longer editing. The separate arrow button on the far right
sends the prompt.

Before sending:

1. Confirm the selected node and profile.
2. Add any needed attachments or sealed values.
3. Review the prompt in the inline field or full composer.
4. Press Send once.

## Ask For A Guided Tour

Try: **“Show the main action row and point out Attach, Files, the prompt box,
the full composer, and Send.”** The agent can place several bubbles at once;
they remain visible for about 30 seconds and do not need to open each
destination.

Related: `understand-the-status-bar.md` and
`ask-an-agent-to-open-the-right-ui.md`.
