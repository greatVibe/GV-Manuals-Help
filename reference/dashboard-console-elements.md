# Dashboard Console Elements

This reference covers the curated dashboard-console controls people commonly
name and the automatic exact-key system that covers every remaining interactive
element. Each entry says what the element does, why it helps, and how to use it.
Decorative text is outside this list.

## Status Bar

| Element | What it does | Why it is helpful | How to use it |
| --- | --- | --- | --- |
| Connection health | Shows the browser's connection state and opens connection details. | Helps explain delays, reconnects, and stale-looking output. | Click the GreatVibe logo to inspect health details. |
| Node picker | Shows and changes the node that receives console work. | Prevents prompts and recovery actions going to the wrong node. | Click for Quick Access; hold when a fuller node view is available. |
| Profile picker | Chooses the AI profile used for the next prompt. | Lets you match the agent profile to the task. | Click it, then choose an available profile. |
| Model picker | Shows and changes model-related controls when available. | Lets you adjust model, effort, or tone without changing the prompt. | Click the relevant model control and choose an available option. |
| Turn status | Displays the selected console's current activity. | Helps you decide whether to wait, recover, or send new work. | Read it before repeating a prompt or using recovery tools. |
| Git status | Summarises repository state for the selected node. | Makes uncommitted or reviewable work visible from the console. | Click it to open repository details and available actions. |
| Jump to latest | Moves the console to its newest output. | Quickly recovers your place in a long conversation. | Click the downward-arrow control. |
| Toolbox | Opens turn, connection, session, and recovery actions. | Keeps powerful recovery controls available without crowding the status bar. | Click it, then choose the needed action. |
| Stop turn | Interrupts the active turn on the selected node. | Lets you safely stop work that should not continue. | Open the toolbox, confirm the node, then click Stop turn once. |
| Turn timer | Shows elapsed time while a turn is active. | Helps distinguish continuing work from an idle console. | Read it together with Turn status. |

## Main Action Row And Prompt

| Element | What it does | Why it is helpful | How to use it |
| --- | --- | --- | --- |
| Main row toggle | Shows or hides the console's main action cards. | Keeps common context and workspace tools close to the prompt. | Click the plus button beside the prompt. |
| Attach | Adds images or files to the next prompt. | Gives the agent the source material it needs. | Reveal the main row and click Attach; hold for more attachment choices. |
| Sealed Secret | Adds a protected value through the sealed-secret flow. | Keeps sensitive values out of ordinary prompt text. | Reveal the main row and click Sealed Secret; hold for advanced options. |
| History | Opens earlier prompts and saved scripts. | Makes useful requests easy to reuse. | Reveal the main row and click History; hold for saved Scripts. |
| Files | Opens files for the selected node. | Lets you inspect and choose workspace material without leaving the console. | Reveal the main row and click Files; hold for the full Files view. |
| IDE | Opens the IDE workspace. | Provides a focused workspace for code and file work. | Reveal the main row and click IDE; hold for gvAPI when available. |
| ChitChat | Opens live mesh messaging. | Helps you communicate and follow collaboration from the console. | Reveal the main row and click ChitChat. |
| Settings | Opens settings for the selected node. | Keeps node-specific configuration close to the current workspace. | Reveal the main row and click Settings; hold for the full Settings view. |
| Prompt input | Holds the request that will be sent to the selected node and profile. | Gives you a final place to write and review the request. | Click the field, enter the request, and review it before sending. |
| Composer | Opens the larger prompt editor. | Makes long or formatted prompts easier to prepare. | Click the composer control inside the prompt area. |
| Send prompt | Sends the prepared request. | Starts the turn only after the prompt and destination are ready. | Confirm node, profile, prompt, and attachments, then click Send once. |

## Support Surfaces

| Element | What it does | Why it is helpful | How to use it |
| --- | --- | --- | --- |
| Support queue | Collects the support requests you are allowed to see. | Gives one place to find and follow reported issues. | Open Support and browse the queue. |
| Support filter | Narrows the visible support request list. | Helps find a request quickly in a larger queue. | Enter a word or identifier in the filter field. |
| Support request | Represents one request in the queue. | Keeps its summary, state, and ownership together. | Select the request to inspect its details. |
| Support actions | Offers actions that are valid for the selected request. | Makes the next available lifecycle step clear. | Choose the action that matches what you need to do. |
| Support evidence | Shows privacy-safe files or screenshots attached to a request. | Provides context for understanding and verifying the issue. | Open a request and review its Evidence section. |
| Support history | Shows recorded changes and updates for a request. | Makes progress and prior decisions easier to follow. | Open a request and read its History section. |
| Support editor | Provides fields for creating or updating a request. | Helps capture a clear, structured support report. | Complete the visible fields, review them, then submit the form. |

## Toolbox Actions

Open the Toolbox before pointing to one of these nested controls. Toolbox is a
distinct surface from Settings; agents must never substitute one for the other.

| Element | What it does | Why it is helpful | How to use it |
| --- | --- | --- | --- |
| Force idle | Clears stale local running chrome. | Recovers the browser display after work has already stopped. | Open Toolbox and click Force idle only when the active work is no longer running. |
| Browser Health | Opens connection and timing diagnostics. | Helps explain stale output, reconnects, and delivery delays. | Open Toolbox and click Browser Health. |
| Reconnect | Rebuilds live console connections. | Restores streaming after a confirmed connection problem. | Open Toolbox and click Reconnect once. |
| Reset console history | Clears browser history caches and fetches authoritative history. | Repairs stale or incomplete local replay without deleting server history. | Open Toolbox and click Reset console history. |
| Access Tree | Opens the organisation, mesh, and node access view. | Shows where the selected node sits and what is available. | Open Toolbox and click Access Tree. |
| New session | Starts fresh context for the selected profile. | Separates new work from the current conversation context. | Open Toolbox, confirm the node and profile, then click New session. |
| Reload | Reloads the dashboard tab. | Restarts the browser shell when lighter recovery actions are insufficient. | Open Toolbox and click Reload only after preserving any draft. |

## Attachment Choices

| Element | What it does | Why it is helpful | How to use it |
| --- | --- | --- | --- |
| Camera | Opens the device camera picker. | Adds a new photo directly to the prompt. | Open Attach, then choose Camera and complete the device picker. |
| Gallery | Opens the image gallery picker. | Adds an existing image to the prompt. | Open Attach, then choose Gallery and select an image. |
| File | Opens the file picker. | Adds a document or other supported file. | Open Attach, then choose File and select it. |
| Paste | Reads supported clipboard content. | Adds copied text or images without browsing files. | Open Attach, then choose Paste and approve clipboard access if asked. |

## History Actions

| Element | What it does | Why it is helpful | How to use it |
| --- | --- | --- | --- |
| Popular | Sorts prompt history by reuse. | Surfaces frequently useful requests. | Open History and click Popular. |
| Latest | Returns history to chronological order. | Makes recent prompts easy to find again. | Open History and click Latest. |
| Clear history | Clears the browser's prompt-history list. | Removes old local suggestions you no longer need. | Open History, click Clear history, and confirm if asked. |

## Files Controls

| Element | What it does | Why it is helpful | How to use it |
| --- | --- | --- | --- |
| Up | Moves to the parent folder. | Navigates a file tree without typing a path. | Open Files and click Up. |
| Home | Returns to the Files home location. | Gives a reliable starting point after deep navigation. | Open Files and click Home. |
| Volumes | Opens available roots and volumes. | Lets you change the file-system area being browsed. | Open Files and click Volumes, then choose an available location. |
| Sort | Opens file ordering choices. | Makes large folders easier to scan. | Open Files, click Sort, then choose a field. |
| Search | Shows or focuses file search. | Finds entries without manually scanning the folder. | Open Files, click Search, and enter a term. |
| Upload | Opens a local file picker for upload. | Adds a local file to the selected node. | Open Files, click Upload, and select a file. |
| Preview | Shows or hides the preview pane. | Lets you inspect a file before selecting or opening it. | Open Files and click Preview. |

## Automatic Exact Coverage

Konui indexes every live button, input, textarea, selector, link, disclosure,
menu item, tab, editable control, declared click action, and custom focusable
control immediately before guidance is placed. It assigns a bounded exact key
using this order:

1. A curated semantic guidance anchor, or an exact-key normalization of an
   internal anchor.
2. The element's stable DOM ID.
3. A bounded action attribute such as tray action, attachment type, tab, sort,
   filter, or IDE action.
4. Its accessible name, title, or visible label.
5. A bounded structural path when the control is icon-only and has no label.

The live catalogue gives every control a target, label, control kind, visibility
state, disabled state, and short use instruction. Exact targets start with
control:, such as control:dash-console-force-idle. They are identifiers, never
selectors. This means dynamically created controls receive the same coverage as
server-rendered controls, and new controls cannot silently fall outside the
guidance system.

## Guidance Marker Index

Agents should read `guidance-markers.md` before using these markers. A marker
may reveal a surface first when its target is otherwise hidden.

<!-- gv-guidance: {"id":"dashboard-connection-health","target":"connection-health","message":"Open browser connection details here when the console looks delayed or stale."} -->
<!-- gv-guidance: {"id":"dashboard-node-picker","target":"node-picker","message":"Choose the node that should receive your next prompt or recovery action here."} -->
<!-- gv-guidance: {"id":"dashboard-profile-picker","target":"profile-picker","message":"Choose the AI profile for your next prompt here."} -->
<!-- gv-guidance: {"id":"dashboard-model-picker","target":"model-picker","message":"Adjust the available model, effort, or tone controls here."} -->
<!-- gv-guidance: {"id":"dashboard-turn-status","target":"turn-status","message":"Check the selected console's current activity here before sending more work."} -->
<!-- gv-guidance: {"id":"dashboard-git-status","target":"git-status","message":"Open repository status and available Git actions here."} -->
<!-- gv-guidance: {"id":"dashboard-jump-latest","target":"jump-latest","message":"Jump to the newest console output with this control."} -->
<!-- gv-guidance: {"id":"dashboard-toolbox","target":"toolbox","message":"Open turn, connection, session, and recovery tools here."} -->
<!-- gv-guidance: {"id":"dashboard-stop-turn","target":"stop-turn","message":"Stop the active turn on the selected node with this control.","surface":"toolbox","action":"stop-turn"} -->
<!-- gv-guidance: {"id":"dashboard-force-idle","target":"force-idle","message":"Clear stale local running chrome with Force idle here.","surface":"toolbox","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-browser-health","target":"browser-health","message":"Open browser connection and timing diagnostics here.","surface":"toolbox","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-reconnect","target":"reconnect","message":"Reconnect the live console and admin connections here.","surface":"toolbox","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-reset-history","target":"reset-history","message":"Clear browser history caches and fetch authoritative console history here.","surface":"toolbox","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-access-tree","target":"access-tree","message":"Open the organisation, mesh, and node access view here.","surface":"toolbox","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-new-session","target":"new-session","message":"Start a fresh session for the selected node and profile here.","surface":"toolbox","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-reload","target":"reload-dashboard","message":"Reload the dashboard tab with this control.","surface":"toolbox","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-turn-timer","target":"turn-timer","message":"See how long the active turn has been running here."} -->
<!-- gv-guidance: {"id":"dashboard-main-row-toggle","target":"main-row-toggle","message":"Show or hide the main console actions with this plus button."} -->
<!-- gv-guidance: {"id":"dashboard-attach","target":"attach","message":"Add images or files to the next prompt here.","surface":"main-row","action":"attach"} -->
<!-- gv-guidance: {"id":"dashboard-attach-camera","target":"attach-camera","message":"Take a new photo for the prompt with this choice.","surface":"attach","action":"camera"} -->
<!-- gv-guidance: {"id":"dashboard-attach-gallery","target":"attach-gallery","message":"Choose an existing image for the prompt with this choice.","surface":"attach","action":"gallery"} -->
<!-- gv-guidance: {"id":"dashboard-attach-file","target":"attach-file","message":"Choose a file for the prompt with this choice.","surface":"attach","action":"file"} -->
<!-- gv-guidance: {"id":"dashboard-attach-paste","target":"attach-paste","message":"Add supported clipboard content with this choice.","surface":"attach","action":"paste"} -->
<!-- gv-guidance: {"id":"dashboard-sealed-secret","target":"sealed-secret","message":"Add a protected value through the sealed-secret flow here.","surface":"main-row","action":"sealed-secret"} -->
<!-- gv-guidance: {"id":"dashboard-history","target":"history","message":"Reuse earlier prompts or open saved Scripts here.","surface":"main-row","action":"history"} -->
<!-- gv-guidance: {"id":"dashboard-history-popular","target":"history-popular","message":"Show frequently reused prompts with Popular.","surface":"history","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-history-latest","target":"history-latest","message":"Return prompt history to chronological order here.","surface":"history","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-history-clear","target":"history-clear","message":"Clear the browser prompt-history list here.","surface":"history","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-files","target":"files","message":"Browse files for the selected node from this action.","surface":"main-row","action":"files"} -->
<!-- gv-guidance: {"id":"dashboard-files-up","target":"files-up","message":"Move to the parent folder with this control.","surface":"files","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-files-home","target":"files-home","message":"Return to the Files home location here.","surface":"files","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-files-volumes","target":"files-volumes","message":"Choose an available root or volume here.","surface":"files","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-files-sort","target":"files-sort","message":"Open file ordering choices here.","surface":"files","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-files-search","target":"files-search","message":"Search the current Files view here.","surface":"files","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-files-upload","target":"files-upload","message":"Upload a local file to the selected node here.","surface":"files","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-files-preview","target":"files-preview","message":"Show or hide the selected file preview here.","surface":"files","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-ide","target":"ide","message":"Open the IDE workspace from this action.","surface":"main-row","action":"ide"} -->
<!-- gv-guidance: {"id":"dashboard-chitchat","target":"chitchat","message":"Open live mesh messaging from this action.","surface":"main-row","action":"chitchat"} -->
<!-- gv-guidance: {"id":"dashboard-settings","target":"settings","message":"Open settings for the selected node from this action.","surface":"main-row","action":"settings"} -->
<!-- gv-guidance: {"id":"dashboard-prompt-input","target":"prompt-input","message":"Write and review the next request in this prompt field."} -->
<!-- gv-guidance: {"id":"dashboard-composer","target":"composer","message":"Open the larger prompt composer here for longer or formatted requests."} -->
<!-- gv-guidance: {"id":"dashboard-send-prompt","target":"send-prompt","message":"Send the reviewed prompt to the selected node and profile here."} -->
<!-- gv-guidance: {"id":"dashboard-support-queue","target":"support-queue","message":"Find the support requests you are allowed to see in this queue.","surface":"support","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-support-filter","target":"support-filter","message":"Narrow the visible support requests with this filter.","surface":"support","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-support-request","target":"support-request","message":"Select a support request here to inspect its details.","surface":"support","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-support-actions","target":"support-actions","message":"Use the available lifecycle actions for this support request here.","surface":"support","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-support-evidence","target":"support-evidence","message":"Review privacy-safe files and screenshots for this request here.","surface":"support","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-support-history","target":"support-history","message":"Follow recorded changes and updates for this support request here.","surface":"support","action":"default"} -->
<!-- gv-guidance: {"id":"dashboard-support-editor","target":"support-editor","message":"Create or update a structured support request in this editor.","surface":"support","action":"default"} -->

## Coverage Rule

This page is complete when every curated target in the live guidance tool
vocabulary appears once in the tables and marker index, and the automatic
catalogue proves that every rendered interactive control receives a non-empty
exact key and use instruction. When the dashboard adds a common named workflow,
promote its exact key to a curated alias and add its marker here.

Sanitization review: the page contains only public element names, user-facing
behaviour, closed marker names, and neutral usage instructions. It contains no
credentials, private routes, customer data, or internal infrastructure details.
