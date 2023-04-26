# Text and Tweet Preprocessing package



This package is created by Behdad (Ben) Ehsani. The package is designed for cleaning tweets on Twitter immediately and with one-shot coding. Additionally, some functions can be used for text preprocessing. An example is provided to demonstrate efficient usage.


## Installing the library

`pip install tweetben==0.0.1`

## Unistalling the library

`pip uninstall tweetben`

## Functions
Here is the list of functions in the library:

1. word_counts(x): Returns the word count of a given text.
2. char_counts(x): Returns the character count of a given text, excluding spaces.
3. avg_wordlength(x): Returns the average word length in a given text.
4. stopwords_count(x): Returns the count of stopwords in a given text.
5. hashtag_couts(x): Returns the count of hashtags in a given text.
6. mention_couts(x): Returns the count of mentions in a given text.
7. digit_counts(x): Returns the count of digits in a given text.
8. uppercase_count(x): Returns the count of uppercase words in a given text.
9. cont_to_exp(x): Expands contractions in a given text.
10. emails(x): Returns the count of emails and a list of emails found in a given text.
remove_emails(x): Removes emails from a given text.
urls(x): Returns the count of URLs and a list of URLs found in a given text.
remove_urls(x): Removes URLs from a given text.
remove_rt(x): Removes the "RT" retweet indicator from a given text.
remove_special_chars(x): Removes special characters from a given text.
remove_html_tags(x): Removes HTML tags from a given text.
remove_accented_chars(x): Removes accented characters from a given text.
remove_stopwords(x): Removes stopwords from a given text.
make_base(x): Lemmatizes a given text, converting words to their base form.
remove_common_words(x, n=20): Removes the n most common words from a given text.
remove_rare_words(x, n=20): Removes the n least common words from a given text.
spelling_checking(x): Corrects spelling errors in a given text using TextBlob.



## Practical Example
Example of one-shot cleaning the code: 

```
import preprocessing_text_ben as pp

def get_clean(x):
    
    # Convert the string to lowercase
    x = str(x).lower()
    
    # Expand contractions like "don't" to "do not"
    x = pp.cont_to_exp(x)
    
    # Remove any email addresses from the string
    x = pp.remove_emails(x)
    
    # Remove any URLs from the string
    x = pp.remove_urls(x)
    
    # Remove any HTML tags from the string
    x = pp.remove_html_tags(x)
    
    # Remove any retweet tags (RT) from the string
    x = pp.remove_rt(x)
    
    # Remove any accented characters from the string
    x = pp.remove_accented_chars(x)
    
    # Remove any special characters from the string
    x = pp.remove_special_chars(x)
    
    # Return the cleaned string
    return x


#here is the cleaned text in one shot
df['your_cleaned_column'] = df['your_text_column'].apply(lambda x: get_clean(x))

```






version: 0.0.1
