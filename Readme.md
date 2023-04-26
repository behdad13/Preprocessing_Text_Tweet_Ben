# Text and Tweet Preprocessing package



This package is created by Behdad (Ben) Ehsani. The package is designed for cleaning tweets on Twitter immediately and with one-shot coding. Additionally, some functions can be used for text preprocessing. An example is provided to demonstrate efficient usage.


## Installing the library

`pip install preprocessing-text-ben`

## Unistalling the library

`pip uninstall preprocessing-text-ben`



Example of one-shot cleaning the code: 

```
import preprocessing-text-ben as pp

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
