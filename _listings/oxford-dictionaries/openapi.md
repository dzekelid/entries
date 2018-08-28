swagger: "2.0"
x-collection-name: Oxford Dictionaries
x-complete: 1
info:
  title: Oxford Dictionaries
  description: if-youre-looking-to-enhance-your-app-or-website-with-dictionary-data-dont-compromise-on-quality--the-oxford-dictionaries-api-offers-easy-and-intuitive-access-to-oxfords-dictionary-content-which-is-trusted-around-the-world--here-at-oxford-dictionaries-home-of-the-oed-we-love-words--thats-why-we-have-experienced-lexicographers-tracking-the-living-language-delving-deep-into-our-corpora-and-monitoring-a-wide-range-of-media-in-order-to-understand-how-words-are-being-used-and-how-language-is-evolving--this-research-is-used-by-our-editors-to-write-and-edit-dictionary-entries-and-translations-meaning-were-able-to-offer-uptodate-accurate-and-reliable-lexical-content-in-multiple-languages-
  termsOfService: http://helloreverb.com/terms/
  version: 1.8.0
host: od-api-demo.oxforddictionaries.com:443
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /entries/{source_language}/{word_id}/sentences:
    get:
      summary: Retrieve corpus sentences for a given word
      description: Use this to retrieve sentences extracted from  corpora which show
        how a word is used in the language. This is available for English and Spanish.
        For English, the sentences are linked to the correct [sense](documentation/glossary?term=sense)
        of the word in the dictionary. In Spanish, they are linked at the [headword](documentation/glossary?term=headword)
        level.
      operationId: getEntriesSourceLanguageWordSentences
      x-api-path-slug: entriessource-languageword-idsentences-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: source_language
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Language
      - Word
      - Id
      - Sentences
  /entries/{source_lang}/{word_id}:
    get:
      summary: Retrieve dictionary information for a given word
      description: Use this to retrieve definitions, [pronunciations](documentation/glossary?term=pronunciation),
        example sentences, [grammatical information](documentation/glossary?term=grammaticalfeatures)
        and [word origins](documentation/glossary?term=etymology). It only works for
        dictionary [headwords](documentation/glossary?term=headword), so you may need
        to use the [Lemmatron](documentation/glossary?term=lemma) first if your input
        is likely to be an [inflected](documentation/glossary?term=inflection) form
        (e.g., 'swimming'). This would return the linked [headword](documentation/glossary?term=headword)
        (e.g., 'swim') which you can then use in the Entries endpoint. Unless specified
        using a region filter, the default lookup will be the Oxford Dictionary of
        English (GB).
      operationId: getEntriesSourceLangWord
      x-api-path-slug: entriessource-langword-id-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
  /entries/{source_lang}/{word_id}/antonyms:
    get:
      summary: Retrieve words that mean the opposite
      description: Retrieve words that are opposite in meaning to the input word ([antonym](documentation/glossary?term=thesaurus)).
      operationId: getEntriesSourceLangWordAntonyms
      x-api-path-slug: entriessource-langword-idantonyms-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Antonyms
  /entries/{source_lang}/{word_id}/regions={region}:
    get:
      summary: Specify GB or US dictionary for English entry search
      description: USe this filter to restrict the lookup to either our Oxford Dictionary
        of English (GB) or New Oxford American Dictionary (US).
      operationId: getEntriesSourceLangWordRegionsRegion
      x-api-path-slug: entriessource-langword-idregionsregion-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: region
        description: Region filter parameter
      - in: path
        name: source_lang
        description: IANA language code
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Regions=region
  /entries/{source_lang}/{word_id}/synonyms:
    get:
      summary: Retrieve words that are similar
      description: Use this to retrieve words that are similar in meaning to the input
        word ([synonym](documentation/glossary?term=synonym)).
      operationId: getEntriesSourceLangWordSynonyms
      x-api-path-slug: entriessource-langword-idsynonyms-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Synonyms
  /entries/{source_lang}/{word_id}/synonyms;antonyms:
    get:
      summary: Retrieve synonyms and antonyms for a given word
      description: Retrieve available [synonyms](documentation/glossary?term=thesaurus)
        and [antonyms](documentation/glossary?term=thesaurus) for a given word and
        language.
      operationId: getEntriesSourceLangWordSynonyms;antonyms
      x-api-path-slug: entriessource-langword-idsynonymsantonyms-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Synonyms;antonyms
  /entries/{source_lang}/{word_id}/{filters}:
    get:
      summary: Apply filters to response
      description: Use filters to limit the [entry](documentation/glossary?term=entry)
        information that is returned. For example, you may only require definitions
        and not everything else, or just [pronunciations](documentation/glossary?term=pronunciation).
        The full list of filters can be retrieved from the filters Utility endpoint.
        You can also specify values within the filter using '='. For example 'grammaticalFeatures=singular'.
        Filters can also be combined using a semicolon.
      operationId: getEntriesSourceLangWordFilters
      x-api-path-slug: entriessource-langword-idfilters-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Filters
  /entries/{source_translation_language}/{word_id}/translations={target_translation_language}:
    get:
      summary: Retrieve translation for a given word
      description: Use this to return translations for a given word. In the event
        that a word in the dataset does not have a direct translation, the response
        will be a [definition](documentation/glossary?term=entry) in the target language.
      operationId: getEntriesSourceTranslationLanguageWordTranslationsTargetTranslationLanguage
      x-api-path-slug: entriessource-translation-languageword-idtranslationstarget-translation-language-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: source_translation_language
        description: IANA language code
      - in: path
        name: target_translation_language
        description: IANA language code
      - in: path
        name: word_id
        description: The source word
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Translation
      - Language
      - Word
      - Id
      - Translations=target
      - Translation
      - Language
  /entries/{source_lang}/{word_id}/definitions:
    get:
      summary: Retrieve only definitions in entry search.
      description: Find available [dictionary entries](/glossary?tag=#entry&expand)
        for given word and language. Filter results by categories.
      operationId: getEntriesSourceLangWordDefinitions
      x-api-path-slug: entriessource-langword-iddefinitions-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Definitions
  /entries/{source_lang}/{word_id}/examples:
    get:
      summary: Retrieve only example sentences in entry search.
      description: Find available [dictionary entries](/glossary?tag=#entry&expand)
        for given word and language. Filter results by categories.
      operationId: getEntriesSourceLangWordExamples
      x-api-path-slug: entriessource-langword-idexamples-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Examples
  /entries/{source_lang}/{word_id}/pronunciations:
    get:
      summary: Retrieve only pronunciations in entry search.
      description: Find available [dictionary entries](/glossary?tag=#entry&expand)
        for given word and language. Filter results by categories.
      operationId: getEntriesSourceLangWordPronunciations
      x-api-path-slug: entriessource-langword-idpronunciations-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Pronunciations
  /entries/{source_lang}/{word_id}/translations={target_lang}:
    get:
      summary: Find translation for a given word.
      description: "Returns target language translations for a given word ID and source
        language. \nIn the event that a word in the dataset does not have a direct
        translation, the response will be a [definition](/glossary?tag=#entry&expand)
        in the target language."
      operationId: getEntriesSourceLangWordTranslationsTargetLang
      x-api-path-slug: entriessource-langword-idtranslationstarget-lang-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: word_id
        description: An Entry identifier
      responses:
        200:
          description: OK
      tags:
      - Entries
      - Source
      - Lang
      - Word
      - Id
      - Translations=target
      - Lang