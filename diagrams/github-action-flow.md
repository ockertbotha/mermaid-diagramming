# GitHub Action: Convert Mermaid Diagrams In Markdown To SVG

```mermaid
flowchart TB
    start([start])
    create[\Create diagram in markdown\]
    commit(Commit changes)
    push(Push changes to GitHub)

    start --> create
    create --> commit
    commit --> push

    subgraph action[GitHub Action]
      direction LR

      subgraph ubuntu-latest
        direction LR
        checkout(Checkout main branch)
        generate(Generate SVG diagrams)
        auto-commit(Auto commit diagrams)

        push --> checkout
        checkout --> generate
        generate --> auto-commit

      end
    end

    finnish([finnish])
    auto-commit --> finnish

```