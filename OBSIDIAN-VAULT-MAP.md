# Obsidian Vault Map

이 문서는 `pm-skills-guide` 의 repo guide 문서를 Obsidian note pack과 어떻게 대응시키는지 정리한다.

## 출력 모드

- mode: `hybrid`
- repo guide: `pm-skills-guide/`
- repo-local note pack: `obsidian/pm skills Guide/`
- live vault target: `unset`
- live sync status: `not applied`

## 안전 원칙

- repo-local pack이 정본이다.
- live vault sync는 **의도된 vault target이 명시적으로 확인된 뒤에만** 수행한다.
- default vault나 CLI 반환값은 참고 정보일 뿐, 목적지 확정 근거가 아니다.

## 매핑

| repo guide | note pack |
|---|---|
| `README.md` | `pm skills Guide/pm skills Guide - MOC.md` |
| `01-learning-paths.md` | `pm skills Guide/02 Learning Paths.md` |
| `02-glossary.md` | `pm skills Guide/03 Glossary.md` |
| `categories/overview.md` | `pm skills Guide/01 Overview.md` |
| `categories/pm-data-analytics.md` | `pm skills Guide/Categories/Pm data analytics.md` |
| `categories/pm-execution.md` | `pm skills Guide/Categories/Pm execution.md` |
| `categories/pm-go-to-market.md` | `pm skills Guide/Categories/Pm go to market.md` |
| `categories/pm-market-research.md` | `pm skills Guide/Categories/Pm market research.md` |
| `categories/pm-marketing-growth.md` | `pm skills Guide/Categories/Pm marketing growth.md` |
| `categories/pm-product-discovery.md` | `pm skills Guide/Categories/Pm product discovery.md` |
| `categories/pm-product-strategy.md` | `pm skills Guide/Categories/Pm product strategy.md` |
| `categories/pm-toolkit.md` | `pm skills Guide/Categories/Pm toolkit.md` |

## note map 의도

- MOC가 frontdoor 역할을 한다.
- Learning Paths / Glossary가 기본 3축이 된다.
- deep dive는 source-backed reading surface로 붙인다.
- References와 Workflows는 길찾기/증거를 붙잡아 둔다.
