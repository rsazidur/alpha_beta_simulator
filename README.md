# Alpha-Beta Pruning Visual Simulator

An interactive tool I built to understand **Minimax and Alpha-Beta Pruning** more easily.

## Why I Built This

While learning Alpha-Beta Pruning, I found it a little confusing to keep track of all the variables, especially `v`, `v'`, `α`, and `β`, and understand why their values change during the algorithm.

So I decided to build something that would let me follow the entire process step by step, rather than just seeing the final answer.

I built this using **HTML, CSS, and JavaScript with the help of Claude (AI)**. I tried to follow the same MAXVALUE and MINVALUE pseudocode taught in class.

My main goal was to make the simulation simple enough for anyone to understand, even if they're completely new to Alpha-Beta Pruning.

## Features

- **Step-by-step simulation:** Follow the algorithm one operation at a time.
- **Live variable tracking:** See how `v`, `v'`, `α`, and `β` change throughout the search.
- **Explanations:** Understand why a value changes, why it stays the same, and when pruning occurs.
- **Custom trees:** Create your own MAX/MIN nodes, add branches, and enter different leaf values.
- **Pruning visualization:** See which branches are skipped and why.
- **Zoomable tree:** Zoom in and navigate larger trees to follow the execution more easily.

## How the Algorithm Works

The simulator follows these conditions from the class pseudocode.

### MAXVALUE

```text
v = -∞

For each child:
    v' = value returned by child

    if v' > v:
        v = v'

    if v' >= β:
        return v

    if v' > α:
        α = v'

return v
```

### MINVALUE

```text
v = +∞

For each child:
    v' = value returned by child

    if v' < v:
        v = v'

    if v' <= α:
        return v

    if v' < β:
        β = v'

return v
```

The simulator shows each comparison, explains whether the condition is true or false, and highlights any updated values or pruned branches.

## How I Developed It

I made several changes while trying to make the simulator easier to follow.

| Stage | What I Wanted | What I Added or Improved |
|---|---|---|
| 1 | Understand all four variables | Line-by-line explanations of `v`, `v'`, `α`, and `β` |
| 2 | Follow the class pseudocode | MAXVALUE and MINVALUE conditions |
| 3 | See the algorithm in action | Interactive step-by-step simulation |
| 4 | Practice different problems | Custom MAX/MIN nodes and editable leaf values |
| 5 | Know why every change happens | Live variable tracking and explanations |
| 6 | Keep the tree visible while simulating | Improved layout and navigation |
| 7 | Make large trees easier to follow | Zoom controls and expanded tree view |
| 8 | Share it with others | Standalone HTML version |

## How to Use

1. Open the simulator in your browser.
2. Load the example tree or create your own.
3. Add MAX/MIN nodes and enter leaf values.
4. Click **Next Step** to follow the algorithm.
5. Watch the values of `v`, `v'`, `α`, and `β` update.
6. Read the explanations to understand each comparison and pruning decision.

You can also download the HTML file and open it locally in a browser.

## Limitations

The simulation logic works well in the examples I've tested, but there are still some frontend issues that I haven't fixed yet.

Since I mainly built this to understand Alpha-Beta Pruning myself, I focused more on the algorithm, variable tracking, and explanations than on polishing the interface.

## Technologies Used

- HTML
- CSS
- JavaScript
- Claude (AI-assisted development)

## Final Note

This isn't a formal course project. It's just something I built while trying to understand Alpha-Beta Pruning better.

Hopefully, it can also help others who find the algorithm confusing at first.
