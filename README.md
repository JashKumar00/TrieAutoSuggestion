# Trie Auto-Suggestion System (Java GUI)

A Java Swing-based auto-suggestion application using a **Trie data structure**. It suggests the top 3 words based on a given prefix, ranked by frequency.

## Features

- **Trie-based prefix search** for fast word lookup
- **Top 3 suggestions** sorted by frequency (descending) and alphabetically on tie
- **Frequency learning** — selecting a word increases its frequency for future suggestions
- **Persistent dictionary** — loads from and saves to `dictionary.txt`
- **Java Swing GUI** — clean desktop interface with input field, suggestion list, and buttons

## Files

- `TrieAutoSuggestionGUI.java` — Main source file containing:
  - `TrieNode` — Individual trie node with children array, word, and frequency
  - `Trie` — Core trie logic: insert, suggest, collect, save/load
  - `TrieAutoSuggestionGUI` — Swing GUI application
- `dictionary.txt` — Pre-loaded word dictionary with frequency counts

## How to Run

### Compile

```bash
javac TrieAutoSuggestionGUI.java
```

### Run

```bash
java TrieAutoSuggestionGUI
```

> Make sure `dictionary.txt` is in the same directory as the compiled class files.

## Usage

1. Type a prefix in the input field
2. Click **Search Suggestions** to see the top 3 matching words
3. Select a word from the list and click **Select Word** to boost its frequency
4. Click **Save & Exit** to persist frequency updates back to `dictionary.txt`

## Dictionary Format

Each line in `dictionary.txt` follows the format:

```
word frequency
```

Example:
```
the 5000
and 2600
to 2800
```

## Data Structures Used

- **Trie** (Prefix Tree) for O(L) prefix search where L = prefix length
- **HashMap** for O(1) dictionary frequency lookups
- **ArrayList** with custom comparator for sorting suggestions
