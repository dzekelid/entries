---
name: Oxford Dictionaries
x-slug: oxford-dictionaries
description: If you&rsquo;re looking to enhance your app or website with dictionary
  data, don&rsquo;t compromise on quality. The Oxford Dictionaries API offers easy
  and intuitive access to Oxfords dictionary content, which is trusted around the
  world. Here at Oxford Dictionaries, home of the OED, we love words. That&rsquo;s
  why we have experienced lexicographers tracking the living language, delving deep
  into our corpora and monitoring a wide range of media in order to understand how
  words are being used and how language is evolving. This research is used by our
  editors to write and edit dictionary entries and translations, meaning we&rsquo;re
  able to offer up-to-date, accurate, and reliable lexical content in multiple languages.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Entries
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/apis.md
specificationVersion: "0.14"
apis:
- name: Oxford Dictionaries - Retrieve corpus sentences for a given word
  x-api-slug: entriessource-languageword-idsentences-get
  description: Use this to retrieve sentences extracted from  corpora which show how
    a word is used in the language. This is available for English and Spanish. For
    English, the sentences are linked to the correct [sense](documentation/glossary?term=sense)
    of the word in the dictionary. In Spanish, they are linked at the [headword](documentation/glossary?term=headword)
    level.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-languageword-idsentences-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-languageword-idsentences-get-openapi.md
- name: Oxford Dictionaries - Retrieve dictionary information for a given word
  x-api-slug: entriessource-langword-id-get
  description: Use this to retrieve definitions, [pronunciations](documentation/glossary?term=pronunciation),
    example sentences, [grammatical information](documentation/glossary?term=grammaticalfeatures)
    and [word origins](documentation/glossary?term=etymology). It only works for dictionary
    [headwords](documentation/glossary?term=headword), so you may need to use the
    [Lemmatron](documentation/glossary?term=lemma) first if your input is likely to
    be an [inflected](documentation/glossary?term=inflection) form (e.g., 'swimming').
    This would return the linked [headword](documentation/glossary?term=headword)
    (e.g., 'swim') which you can then use in the Entries endpoint. Unless specified
    using a region filter, the default lookup will be the Oxford Dictionary of English
    (GB).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-id-get-openapi.md
- name: Oxford Dictionaries - Retrieve words that mean the opposite
  x-api-slug: entriessource-langword-idantonyms-get
  description: Retrieve words that are opposite in meaning to the input word ([antonym](documentation/glossary?term=thesaurus)).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idantonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idantonyms-get-openapi.md
- name: Oxford Dictionaries - Specify GB or US dictionary for English entry search
  x-api-slug: entriessource-langword-idregionsregion-get
  description: USe this filter to restrict the lookup to either our Oxford Dictionary
    of English (GB) or New Oxford American Dictionary (US).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idregionsregion-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idregionsregion-get-openapi.md
- name: Oxford Dictionaries - Retrieve words that are similar
  x-api-slug: entriessource-langword-idsynonyms-get
  description: Use this to retrieve words that are similar in meaning to the input
    word ([synonym](documentation/glossary?term=synonym)).
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idsynonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idsynonyms-get-openapi.md
- name: Oxford Dictionaries - Retrieve synonyms and antonyms for a given word
  x-api-slug: entriessource-langword-idsynonymsantonyms-get
  description: Retrieve available [synonyms](documentation/glossary?term=thesaurus)
    and [antonyms](documentation/glossary?term=thesaurus) for a given word and language.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idsynonymsantonyms-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idsynonymsantonyms-get-openapi.md
- name: Oxford Dictionaries - Apply filters to response
  x-api-slug: entriessource-langword-idfilters-get
  description: Use filters to limit the [entry](documentation/glossary?term=entry)
    information that is returned. For example, you may only require definitions and
    not everything else, or just [pronunciations](documentation/glossary?term=pronunciation).
    The full list of filters can be retrieved from the filters Utility endpoint. You
    can also specify values within the filter using '='. For example 'grammaticalFeatures=singular'.
    Filters can also be combined using a semicolon.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idfilters-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idfilters-get-openapi.md
- name: Oxford Dictionaries - Retrieve translation for a given word
  x-api-slug: entriessource-translation-languageword-idtranslationstarget-translation-language-get
  description: Use this to return translations for a given word. In the event that
    a word in the dataset does not have a direct translation, the response will be
    a [definition](documentation/glossary?term=entry) in the target language.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-translation-languageword-idtranslationstarget-translation-language-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-translation-languageword-idtranslationstarget-translation-language-get-openapi.md
- name: Oxford Dictionaries - Retrieve only definitions in entry search.
  x-api-slug: entriessource-langword-iddefinitions-get
  description: Find available [dictionary entries](/glossary?tag=#entry&expand) for
    given word and language. Filter results by categories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-iddefinitions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-iddefinitions-get-openapi.md
- name: Oxford Dictionaries - Retrieve only example sentences in entry search.
  x-api-slug: entriessource-langword-idexamples-get
  description: Find available [dictionary entries](/glossary?tag=#entry&expand) for
    given word and language. Filter results by categories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idexamples-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idexamples-get-openapi.md
- name: Oxford Dictionaries - Retrieve only pronunciations in entry search.
  x-api-slug: entriessource-langword-idpronunciations-get
  description: Find available [dictionary entries](/glossary?tag=#entry&expand) for
    given word and language. Filter results by categories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idpronunciations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idpronunciations-get-openapi.md
- name: Oxford Dictionaries - Find translation for a given word.
  x-api-slug: entriessource-langword-idtranslationstarget-lang-get
  description: "Returns target language translations for a given word ID and source
    language. \nIn the event that a word in the dataset does not have a direct translation,
    the response will be a [definition](/glossary?tag=#entry&expand) in the target
    language."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/oxford-dictionaries-api.png
  humanURL: https://developer.oxforddictionaries.com/
  baseURL: https://od-api-demo.oxforddictionaries.com:443//api/v1
  tags: dictionaries, Words, General Data, Service API, Pedestal
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idtranslationstarget-lang-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/entries/master/_listings/oxford-dictionaries/entriessource-langword-idtranslationstarget-lang-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://orghunter.api.gallery.streamdata.io
- type: x-api-stack
  url: http://oxford.dictionaries.stack.network
- type: x-blog
  url: https://api-blog.oxforddictionaries.com/
- type: x-developer
  url: https://developer.oxforddictionaries.com/
- type: x-faq
  url: https://developer.oxforddictionaries.com/faq
- type: x-forum
  url: https://forum.oxforddictionaries.com/api/
- type: x-twitter
  url: https://twitter.com/OxfordWordsAPI
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---