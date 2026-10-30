# Pitch Timer

**AppADay 176** | Creative | Claude API

Enter your current role, a few lines of background, and the job you want, and Claude drafts a tight elevator pitch built in four parts: a hook, why it matters to the listener, one proof point, and a clear ask. Edit it with a live word count and speaking time estimate, then rehearse out loud against a countdown that shifts green to amber to red, keeps counting past zero, and logs every run against your target.

## How to use it

**Connect your key.** The first time you draft, a sheet slides up offering to restore your keys from your AppADay key file or to enter a key. You can also do this any time from the gear in the header, which shows whether this app uses its own key or your default key (last four characters only) and lets you enter a key, restore from or back up to your key file, or forget a key. Get a key at [console.anthropic.com](https://console.anthropic.com/).

**Tell it about you.** Fill in Current role, Target job, and Background (skills, a result you are proud of, numbers if you have them). Choose who is listening (Recruiter, Hiring manager, Networking, or Career fair), a tone (Confident, Warm, or Direct), and a length of 30, 45, or 60 seconds. Try an example fills in a sample so you can see how it works. Tap Draft my pitch.

**Tighten it.** The pitch lands in an editable box. Below it, a meter shows the word count, the estimated speaking time at your chosen pace (Measured 130, Natural 150, or Brisk 170 words per minute), and whether you are on target or how many words to trim or add. How this draft is built shows the hook, relevance, proof, and ask Claude used. Regenerate pitch draws a fresh version with your current settings, and Previous draft swaps back if you liked the last one better. Claude is told to use only facts from your background and never to invent numbers, employers, or credentials.

**Rehearse.** Tap Start (or press Space on a keyboard) and say the pitch out loud. The ring drains green, turns amber in the last third, and turns red at zero, where the clock flips to counting up so you see exactly how far over you ran. A chime and a buzz mark the target time; turn them off in Settings. Tap Stop and log to record the run, or Discard run to toss it. Runs under 2 seconds are ignored. Hide script lets you practice from memory, and Stage mode fills the screen with the timer and script for practicing on a phone. The screen stays awake while the timer runs where the browser supports it.

**Track your runs.** Practice runs lists your last 8 runs with a bar against the target marker, whether the script was shown, and the pace you would have needed to say every word. The stats show the average of your last 5 runs, the run closest to target, and how many runs landed on target (within 7 percent, and never less than 2 seconds). The last 20 runs are kept.

**Take it with you.** Copy pitch puts the text on your clipboard. Download .md saves elevator-pitch.md with the pitch, its structure, its length, and your practice runs. Clear everything in Settings removes your details, pitch, and runs but leaves your API key alone.

## API key

Key handling comes from the shared AppADay key ring, [keys.js](https://augustineiacopelli.github.io/appaday/keys.js), described in KEYS.md in the portal repo. The key lives under appaday.key.176 with a fallback to your default key, and can be backed up to a passphrase encrypted file, appaday-keys.json, that restores every AppADay app's key at once.

## Privacy

Your API key, your details, your pitch, and your practice runs are stored only in this browser's localStorage. The key and your details are sent directly from your browser to api.anthropic.com and nowhere else. Nothing is recorded; the timer never uses the microphone.

## Model

The model is not hardcoded. The app asks the portal's shared models.js for the haiku tier, which follows the AppADay central [config.json](https://augustineiacopelli.github.io/appaday/config.json). A short pitch does not need a larger model, which keeps each draft fast and inexpensive. Thinking is turned off with a per model fallback so the full token budget goes to the pitch, and a draft that comes back far from the target length is retried once.

## Links

Live app: https://augustineiacopelli.github.io/appaday-176-pitch-timer/

Portfolio: https://augustineiacopelli.github.io/appaday/
