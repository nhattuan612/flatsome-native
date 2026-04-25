# Factory Overview

Date: 2026-04-23

## Purpose

This folder turns the Flatsome platform knowledge into reusable production patterns.

`Platform` answers:

- what shortcode exists
- what syntax works
- what Studio template maps to what `templateId`

`Factory` answers:

- what section to assemble for a real page
- what variables to swap
- what section order fits a page goal
- what design language to borrow from
- how to avoid repeating the previous page layout
- what layout pool to force before build
- what hero family rotation is safest next
- what starter shell to use after route is locked

## Factory rule

- platform stays domain-agnostic
- factory stays reusable across many projects
- project naming, brand copy, and media belong in `project profiles`

## Main assets

- `03-factory/Section Archetypes.md`
- `03-factory/Section Starter Snippets.md`
- `03-factory/Composition Rules.md`
- `03-factory/Block Registry.md`
- `03-factory/Page Goal Routing.md`
- `03-factory/Block Library Candidates.md`
- `03-factory/Design Language Reference.md`
- `03-factory/Layout DNA.md`
- `03-factory/Layout Pool.md`
- `03-factory/Hero Family Matrix.md`
- `03-factory/No Repeat Law.md`
- `03-factory/Section Order Recipes.md`
- `03-factory/Typography System.md`
- `03-factory/Spacing System.md`

## Usage

1. start from `01-platform/Native Builder Language Map.md`
2. inspect `02-platform-studio-library/` for candidate source templates
3. route the brief with `03-factory/Page Goal Routing.md`
4. choose design direction from `03-factory/Design Language Reference.md`
5. if stronger creativity is needed, route through `08-design-intelligence/Design Mode Router.md`
6. lock typography with `03-factory/Typography System.md`
7. lock spacing with `03-factory/Spacing System.md`
8. lock `03-factory/Layout DNA.md`
9. choose `03-factory/Layout Pool.md`
10. rotate hero with `03-factory/Hero Family Matrix.md`
11. check `03-factory/No Repeat Law.md` and choose a `Section Order Recipe`
12. compare against `07-reports/Recent Page Memory.md`
13. choose archetypes from this factory
14. open `03-factory/Section Starter Snippets.md` for the nearest starter shell
15. decide `reuse existing block / create new / page-only block`
16. check `03-factory/Block Library Candidates.md` and `03-factory/Block Registry.md` before creating a new reusable block
17. adapt variables for the target project profile
18. output shortcode-native content that still opens in UX Builder

## Factory Handshake Rule

Factory không được bàn giao sang `Page Plan` nếu còn thiếu một trong các mục:

- `Skeleton`
- `Archetype`
- `Section starter direction`
- `Block reuse decision`

Nếu task thuộc nhánh creative:

- phải có thêm `Design Mode`
- `Style family`
- `Pattern family`
