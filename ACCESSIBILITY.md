# Accessibility

The Mosgird Android app is meant to be usable by everyone, including people who use TalkBack or another screen reader, switch access, magnification or large text, and people who need reduced motion or high contrast.

## Target

We aim to meet WCAG 2.2 Level AA for the app's user interface. This is a target, not a claim. The app does not claim conformance until it has been tested against the criteria, and the results are published with the release.

## What the app is built to do

- Every control can be reached and operated with TalkBack, switch access, and a hardware keyboard, with a visible focus indicator and a logical focus order.
- Every control has a content description, role, and state, using Android's accessibility APIs.
- Information is never conveyed by color alone.
- Text follows the system font size, and layouts keep working at the largest size without losing content or function.
- The app respects the system's reduced-motion setting, and nothing flashes more than three times per second.
- Errors are announced to assistive technology and explained in text.
- Text and interface components meet the WCAG AA contrast ratios, in light and dark themes.
- Images and icons shipped with the app have text alternatives. Assets are made by people, not AI tools (see [AI_POLICY.md](AI_POLICY.md) in mosgird/protocols).

## Testing

Each release is tested with TalkBack and with switch access on at least one current and one older Android version, and with the largest system font size. Automated checks, such as the Android accessibility scanner, are a first step, not a replacement for those tests.

## Reporting an accessibility problem

Open an issue and add the `accessibility` label. Describe the Android version, the device, the assistive technology you used, and the steps that failed. An accessibility problem is not a security problem; report security problems as described in [SECURITY.md](SECURITY.md).

## Status

No user interface exists yet. This document states intent for the app. It does not describe current behavior.
