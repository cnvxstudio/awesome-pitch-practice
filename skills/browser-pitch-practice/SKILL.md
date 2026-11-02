---
name: browser-pitch-practice
description: Guide a short singing pitch-practice session in AI Voice Coach, choose a suitable exercise, and turn the user's visible pitch observations into one useful next attempt.
---

# Browser pitch practice

Help someone practise one small singing skill at a time using AI Voice Coach. This is a text-only practice guide maintained by the product team; it does not implement pitch detection or access a microphone.

## Choose one useful exercise

Start with the user's stated goal and available time. If unclear, offer these choices rather than a long questionnaire:

- **Find a note:** use Single note to hear a reference and compare a comfortable sung or hummed note with the target.
- **Follow a pattern:** use Short melody to practise the order of a small pitch pattern.
- **Observe a held note:** use Long note to watch pitch movement without a target or a right-or-wrong score.
- **Play:** try the voice-control games when the user prefers a game to a drill. Pitch controls the movement; shouting is not the aim.

Direct the user to [AI Voice Coach](https://aivoicecoach.ai/) and the matching visible exercise. Use the current menu labels if they differ. The public [voice-control guide](https://aivoicecoach.ai/voice-control-games) is useful for game instructions. Do not invent exercise URLs or an API.

## Run a short session

For a first session, suggest about three minutes:

1. Let the user choose a comfortable note or range. Play the reference before singing; headphones can reduce reference audio entering the microphone.
2. Ask for one gentle attempt with “la,” “ah,” or a hum. The user starts and stops the exercise themselves and controls microphone permission.
3. Ask for the simplest observation relevant to that exercise: above/below/near the target, the order of the melody, or the shape of the held-note trace.
4. Change only one thing for the next attempt. If below the target, try a small upward adjustment; if above, a small downward adjustment. If the reference is uncomfortable, choose another note instead.
5. Finish with one observation and one next step, not a claim that singing ability has been graded.

For a held note, discuss the visible path instead of inventing an accuracy score. A moving trace can be a useful observation without proving a cause. Stop the session if singing becomes painful or uncomfortable.

## Interpret the evidence the user supplies

Use the user's description or an explicitly supplied screenshot. Do not claim to hear their voice, calculate a score, or know the detected pitch unless they actually provide it. Missing trace data is unknown, not zero.

- **No trace / insufficient sound:** check that recording was active during the attempt, microphone permission is allowed, the intended input is selected, and the user is close enough to the mic. Try one short hum after those checks.
- **A trace outside the chart:** explain that the display range was exceeded; it does not establish a vocal problem. Try a comfortable note within the displayed range.
- **A sudden large jump:** ask whether the user changed notes or the trace briefly lost tracking. Do not diagnose breath, tone, or vocal health from a pitch line.
- **A successful attempt:** describe the specific observation, such as “the second attempt stayed closer to the target,” rather than promising general improvement.

No audio upload, credentials, personal details, installation, executable tools, or payment is needed for this guide. It makes no medical or pronunciation assessment.

## Example response

“Let's use Single note for two short attempts. Open AI Voice Coach, pick a comfortable target, listen once, then hum gently. Tell me whether the line sits mostly above, below, or near the target. We'll adjust one thing for the second try.”

A useful finish: “You reported that the line was below the target first and closer on the second attempt. Next time, start with the same comfortable target and repeat that small upward adjustment.”
