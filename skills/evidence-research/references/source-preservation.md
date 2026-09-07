# Source Preservation

Use this workflow when the user needs research that remains traceable if a webpage changes or disappears. Store the evidence package in the research output directory, not inside this skill.

## Package structure

Prefer a small, portable structure:

```text
research-output/
|-- report.md
`-- references/
    |-- sources.csv
    `-- files/
        |-- smith-2025-study.pdf
        `-- agency-2026-guidance.pdf
```

Use stable, descriptive filenames without relying on the publisher's download name. Avoid embedding secrets, query tokens, or personal data in filenames or the source register.

## Source register

Record one row per source in `sources.csv`, or an equivalent machine-readable table appropriate to the deliverable. Include when available:

- a stable source ID used by the report;
- title, authors or issuing organization, and publication date;
- source type, such as journal article, dataset, regulation, filing, official webpage, news article, Medium post, personal blog, or expert commentary;
- canonical URL and a persistent identifier such as DOI, PMID, ISBN, report number, or dataset accession;
- date and time accessed, including timezone;
- version, edition, jurisdiction, or effective date when relevant;
- local relative path and file format for an offline copy;
- cryptographic checksum, preferably SHA-256, for the captured file;
- license or reuse status when known;
- the claim, section, page, table, or figure for which the source was used;
- notes about availability, transformations, missing metadata, or access limitations.

Do not rely on a local filename alone to identify a study. For academic work, capture the article title, authors, venue, year, and DOI or other persistent identifier whenever available.

## Capture by source type

For a PDF, preserve the publisher's original PDF without modifying it. If text extraction, OCR, translation, or annotation is needed, store that as a separate derived file and identify the tool or transformation in the source register. Cite page, figure, or table numbers from the original when possible.

For a webpage, retain the canonical URL and capture date, then prefer a self-contained PDF snapshot when visual layout matters or a clean HTML/Markdown/text snapshot when searchable content matters. Dynamic or interactive pages may need both a visual capture and an extracted text representation. Record omitted interactive elements and the capture method.

For a blog, Medium post, newsletter, or similar informal publication, also preserve the author or account name, publication platform, publication and update dates, author biography or relevant affiliation when material to credibility, and links to any underlying evidence. Label the source type plainly so readers can distinguish practitioner experience or commentary from peer review, official guidance, and independent reporting.

For official technical documentation, record the product, language, framework, runtime, or library version; the documentation version or release channel; the exact page and section; and the related specification, API reference, release note, migration guide, or source repository when relevant. Prefer version-pinned URLs over unversioned `latest` pages. If only rolling documentation exists, record the access date and preserve a snapshot when permitted.

For datasets, preserve the exact downloaded file or a documented subset, along with the dataset version, query parameters, retrieval date, schema, and license. Keep analysis outputs separate from source data.

If copying is not permitted or technically possible, preserve only allowed metadata, the canonical link, relevant citation details, and a note explaining the limitation. A public archive URL may supplement the canonical URL when lawful and available, but should not replace it.

## Integrity and freshness

Compute a SHA-256 checksum after capture and do not overwrite a preserved source when it changes. Save a new dated or versioned copy and update the register instead.

Treat an offline copy as evidence of what was captured at a particular time, not as proof that the source remains current. Revisit the canonical source before making freshness-sensitive claims, and disclose when only the archived copy could be checked.

Before delivery, open a sample of captured files, verify that report citations resolve to the correct register entries, and check that paths are relative and portable. Do not claim an offline package is complete when any consequential source could not be preserved.

## Rights and sensitive material

Keep offline copies private to the user's authorized workspace unless redistribution rights are clear. Do not publish copyrighted papers, paywalled material, personal data, confidential documents, or licensed datasets merely because they were accessible during research. Preserve the minimum material needed for auditability and follow the source's terms and the user's distribution context.
