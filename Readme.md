# Preprocessing python package



This package is created by Behdad (Ben) Ehsani. The package is created for cleaning tweets on Twitter Immidiately and in one-shot coding. Also, some functions can be used for Text Preprocessing. An example is preparedt to how to use it efficiently.


installing library: `pip install preprocessing-text-ben`

Unistalling Library: pip uninstall preprocessing-text-ben

example of one-shot coding: 


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









version: 0.0.1
