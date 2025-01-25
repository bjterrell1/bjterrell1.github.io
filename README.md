```mermaid
flowchart TD
    A[Start] --> B["Generate Random Number (1-100)"]
    B --> C["Prompt User for Guess"]
    C --> D["Is Input Valid?"]
    D -->|No| E["Prompt for Valid Input"]
    D -->|Yes| F["Is Guess Correct?"]
    E --> C
    F -->|Yes| G["Display 'Correct!'"]
    F -->|No| H["Is Guess Too Low?"]
    H -->|Yes| I["Display 'Guess Higher'"]
    H -->|No| J["Display 'Guess Lower'"]
    I --> C
    J --> C
    G --> K["Ask if Play Again?"]
    K -->|Yes| B
    K -->|No| L[End]
