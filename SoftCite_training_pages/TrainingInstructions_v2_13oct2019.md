# Training instructions: Transitioning to TagWorks
_Fan Du, Oct 13, 2019_

## Project Goal
  We are developing a dataset of software mentions in academic texts by annotating the research papers. This dataset will be used for training a machine learning system to automatically recognize software mentions in research papers.  

  **_Note_**
  1. We annotate the mention of a concrete piece of software in its specific text. This is why we are annotating the same software mention (e.g., "MATLAB") in different sentences across many articles. Because the machine learning algorithm is learning the pattern in which the software mentions appear in texts across many examples.
  2. A piece of software may be mentioned in many different ways. e.g., "SPSS", "Social Sciences Statistical Package", "Social Sciences Statistical Package (SPSS)", "SPSS ~~software~~", etc.

## Terminology Clarification
  We have been using "annotate"/"code"/"highlight"/"tag"/(sometimes)"label" interchangeably. They all have the same meaning. When we were working with the command line we used "code" more. "Annotation" is more close to the machine learning terminology especially when talking about text training data generation. "Highlight" is the TagWorks term.

## Changes in Workflow
  Our previous approach is to read full research papers and code the software mentions in .ttl files. The codes we used in the past include: _coded_no_in_text_mentions, codable, standard_type, in_text_mention (full_quote, on_pdf_page, span_pages, mention_type, software_was_used, software_name, version_number, version_date, url, creator, has_reference), reference (full_quote, on_pdf_page, spans_pages, reference_type, software_name, version_number, version_date, url, creator)_.


  **Current workflow on TagWorks**: a 2-phase approach
  ![tagworks workflow](https://github.com/caifand/fandu.github.io/blob/master/SoftCite_training_pages/CrowdAnnotationFlow_13oct2019.png)
    The detail information of a software mention in the text we are annotating in Phase II now:  
      - `software name`  
      - `version`: including both version number and release date. no text included.  
      - `url` (_URL to what?_): software website, project page, repository page, documentation page, etc.  
      - `publisher`: including both individual and organization. Replaces `creator`. Just a title change.  

## Understand TagWorks
  1. Use keyboard shortcuts on TagWorks  
    Case numbers should be auto-incrementing now. We don't need to worry about them. Just remember:  
    - Use "Delete" key to remove wrong highlights on TagWorks.  
    - Hold "Alt" (on Windows)/"Options" (on Mac) for accurate control of word boundary.  
  2. Understand the interface cues on TagWorks (_We will cover this on Friday_)  
    - Task interface: Help and prompts. Inkwell. Review.  
    - Adjudication interface  
  3. Understand the terminology and architecture of TagWorks (_We will cover this on Friday_)  
    - Terminology: project. task. task run. contributor. IAA/consensus processing. adjudicator. highlight/TUA.  

## What do we need to do?
(_We will cover this on Friday_)
  - Adjudication & help improve adjudicator
  - Curate edge cases
  - Monitor existing issues
