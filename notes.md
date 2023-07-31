# Notes

## Why we animate?

- convey the state of the app
  - inform the use about what could happen and what did happen
- style and branding
  - have a consistent feel across the app
  - app feels cohesive
  - gives the user trust

## Fundamentals

- Duration: how long an iteration of an animation takes to complete
- Delay: how long it takes before an animation starts. Only happens once
- Timing: the easing of an animation

Cubic Bezier function

- `cubic-bezier(0.5, 0, 0.5, 1)`
- keep the second number `0` and the last number `1`

What to animate:

- good: transform, opacity. This uses the GPU and is more performant. It does not necessitate a layout shift
- ok: colour and background. Uses the CPU but does not trigger a layout
- not good: height, width, left, right. Triggers a layout and needs to reflow the page and neighbouring elements

60fps is great for animations because that is the monitor refresh rate.

Animation Play State
`animation-play-state: paused` pauses the animation

## Choreography

For nested animations use a container element, since multiple keyframe animations cannot happen on the same element at the same time.
