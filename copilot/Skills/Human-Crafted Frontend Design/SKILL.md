# Frontend Design Skill Spec

## Skill Name

Human-Crafted Frontend Design

## Purpose

Generate frontend UI directions and implementation guidance for modern web apps that feel premium, calm, readable, and intentionally designed.

This skill helps produce interfaces that avoid the AI-generated look by emphasizing content, typography, hierarchy, restraint, and real product thinking.

## When to Use

Use this skill when:

* designing a new frontend screen or app shell
* improving an existing UI to feel more modern
* generating layout and styling instructions for another agent
* defining a design system for a web app
* turning product requirements into frontend structure

## Skill Output

The skill should produce:

* UI direction
* layout structure
* component recommendations
* typography system
* spacing system
* color rules
* motion rules
* content hierarchy
* empty/loading/error state guidance
* anti-AI design constraints

## Design Principles

1. Content is the hero.
2. Typography carries the identity.
3. Whitespace creates rhythm and focus.
4. Color is controlled and intentional.
5. Motion is subtle and meaningful.
6. Layout should feel human, not mechanically repetitive.
7. The UI must support real workflows and real product states.
8. Minimalism should improve clarity, not remove usefulness.
9. The interface must feel brand-specific and domain-specific.
10. Avoid generic AI-template aesthetics.

## Default Style Rules

* Use a neutral base palette.
* Prefer black, white, and muted grays.
* Add only one controlled accent if needed.
* Use elegant, highly readable typography.
* Keep spacing disciplined and consistent.
* Favor subtle borders or soft elevation over dramatic shadows.
* Keep motion minimal and functional.
* Avoid decorative clutter and overdesigned effects.

## Anti-Patterns to Reject

* generic centered hero blocks
* repetitive card grids
* excessive gradients
* glassmorphism overload
* loud accent colors everywhere
* symmetrical but lifeless compositions
* placeholder-looking copy
* screens that look polished but lack product logic

## Required Thinking Process

For every screen:

1. identify the user goal
2. identify the decision the screen supports
3. choose the smallest useful layout
4. establish hierarchy through type and spacing
5. verify states and edge cases
6. remove anything ornamental that weakens clarity

## Success Criteria

A successful output should feel:

* clean
* premium
* calm
* confident
* readable
* modern
* product-first
* human-crafted

## Example Behavior

If the user asks for a dashboard, do not produce a generic SaaS dashboard.

Instead, design a dashboard with:

* a clear primary task
* one dominant piece of content
* a compact supporting summary
* a restrained visual system
* a real workflow
* a distinct brand feel

## Optional Instructions for Agent Use

When used by another agent, the agent should:

* follow these rules before generating UI
* never default to generic templates
* justify every visual choice
* optimize for real usage, not visual noise
* keep the final result simple, elegant, and specific to the product
