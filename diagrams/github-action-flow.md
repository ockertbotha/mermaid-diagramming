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
```mermaid
flowchart LR
  subgraph TOP
    direction TB
    subgraph B1
        direction RL
        i1 -->f1
    end
    subgraph B2
        direction BT
        i2 -->f2
    end
  end
  A --> TOP --> B
  B1 --> B2
  ```
  ```mermaid
flowchart TB
    commit --> push
    push --> action
    subgraph action
      direction TB
      subgraph ubuntu-latest
        direction LR
        checkout --> generate
        generate --> auto-commit
      end
    end
    action --> finnish
```