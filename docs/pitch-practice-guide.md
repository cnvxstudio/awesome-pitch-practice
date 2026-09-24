# Pitch Practice in Your Browser: Notes, Cents & Voice Games

This guide explains how to read pitch feedback and run a simple practice session. It is maintained by the maker of [AI Voice Coach](https://aivoicecoach.ai/). The exercises below use that product as a concrete example; the measurement concepts apply more broadly.

## What a pitch detector actually measures

A microphone captures a mixture of sound. A pitch detector tries to estimate the repeating frequency of a pitched sound. The display may then convert that frequency into a note name or a distance from a target.

These are different quantities:

| Quantity | Example | Meaning |
| --- | --- | --- |
| Frequency | 440 Hz | A frequency commonly used as the reference for A4. |
| Note label | A4 | A musical note and octave, under the chosen tuning reference. |
| Pitch difference | +20 cents | Slightly above the target, where a semitone is 100 cents. |
| Detector clarity | A value returned by an algorithm | A signal property used to decide whether an estimate is usable; not a grade for the singer. |

With a target frequency `targetHz` and a detected frequency `detectedHz`, the pitch difference in cents is:

```text
cents = 1200 × log2(detectedHz / targetHz)
```

For example, a detected 440 Hz against a 440 Hz target is 0 cents. A detected 880 Hz is 1200 cents above that target: one octave. This explains why singing the same note name in another octave can still miss a game's target.

A positive difference means higher than the target; a negative difference means lower. A tool chooses its own tolerance for “close,” so scores from different tools are not automatically comparable.

## Start with one note

1. Open [AI Voice Coach](https://aivoicecoach.ai/) and choose **Practice → Single note**.
2. Choose a comfortable target using the available note controls. Listen before trying to match it.
3. Start the take, allow microphone access, and sing or hum a clear sustained sound.
4. Compare your trace with the target and read the result. Adjust the pitch gently on the next attempt.

Try to change one variable at a time. If you change the target, microphone distance, and vowel together, it becomes harder to understand why the result changed.

## Add a short melody

Select **Short melody**, listen to the phrase, and echo its note sequence. In AI Voice Coach, this exercise compares detected notes and their order; it does not require the exact same rhythm.

If a phrase is difficult, return to a single note and get comfortable with the listening and microphone controls. Do not interpret a failed phrase as a judgment of your overall musical ability.

## Observe a long note

Select **Long note** and hold any comfortable pitch. Watch whether the trace stays in one region, rises, falls, or contains gaps.

This exercise has no target pitch or correct answer. It shows movement rather than assigning a singing grade. A changing trace can reflect the sound you made, background interference, or uncertainty in the estimate; the graph alone does not establish the cause.

## Use a voice-control game

Open [Pitch Ninja](https://aivoicecoach.ai/voice-control-games) and choose a comfortable Low, Middle, or High range. Listen to the targets and change your sung pitch to reach them. Aim with pitch, not volume.

The current game has six levels. Later levels use narrower pitch tolerances and different target sequences; each target window remains four seconds. Range selection shifts the target notes without changing the level rules.

Read the result as success at the game's targets in that session. It is not a standardized vocal assessment, and a game score should not be compared with a different product's score as though both measured the same thing.

## Troubleshooting

| What you see | What to check first | What the result does not establish |
| --- | --- | --- |
| Microphone cannot start | Browser permission, operating-system microphone access, and the intended input device. | That your voice is unsuitable. |
| No reliable sound or no pitch trace | Sing one clear note in a quiet room; check whether the selected microphone is receiving you. | A score of zero for your singing. |
| Unexpected notes when external music is playing | Make sure the microphone is not mainly hearing a loud speaker or other music. Headphones can help separate external reference playback from your voice. | That the displayed note came only from your voice. |
| Sudden octave jumps | Try a clearer single tone and reduce competing sound. A detector may follow a different component of the signal. | That your voice necessarily jumped an octave. |
| A stable-looking line still misses a target | Compare the actual note and octave with the target. A stable pitch can still be above or below it. | That stability alone means a correct match. |
| A gap in the curve | Check for silence, low input, or unclear sound. Treat the missing segment as unavailable information. | A measured pitch during the gap. |

Keep practice within a comfortable range and stop if it hurts. The tool provides pitch feedback, not medical advice or a substitute for an individual voice teacher.

## A note for people building pitch tools

Keep raw measurements, validity decisions, and user-facing feedback separate. A clarity threshold is an engineering choice, not a quality score for someone's voice. Silence or an unreliable estimate should remain missing data rather than becoming a fabricated note.

If you use a library such as [Pitchy](https://github.com/ianprime0509/pitchy), read its current API and license. Its frequency and clarity outputs need interpretation appropriate to your application's input and goals.

## Further reading

- [Tool selection and FAQ](../README.md)
- [Official source register and verification limits](../SOURCES.md)
- [Singing Carrots Pitch Monitor](https://singingcarrots.com/pitch-monitor)
- [Musicca tuner explanation](https://www.musicca.com/tuner)
- [Chrome Music Lab Spectrogram](https://musiclab.chromeexperiments.com/Spectrogram/)

Last reviewed: September 23, 2026.
