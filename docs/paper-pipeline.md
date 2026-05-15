# Daily ArXiv Paper Pipeline

## Overview
Automated pipeline for fetching and summarizing latest arXiv papers.

## Pipeline
```
arXiv API → Filter by topic → Extract abstracts → Summarize → Format → Publish
```

## Configuration
```yaml
topics:
  - machine learning
  - NLP
  - computer vision
  - reinforcement learning
max_papers: 15
summary_length: 200  # words
output_format: markdown
schedule: "0 6 * * *"  # Daily at 6 AM UTC
```

## Output Format
```markdown
# Latest {N} Papers - {DATE}

## 1. {Title}
- **Authors**: {First Author} et al.
- **Category**: {Category}
- **Summary**: {2-3 sentence summary}
- **Link**: {arxiv_url}
```

## Summarization
- Uses extractive summarization
- Key contribution highlighted
- No hallucinated content
