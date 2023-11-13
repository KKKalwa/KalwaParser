# KalwaParser

 KalwaParser is a laravel package used to parse xml sitemap.
## Installation

Install KalwaParser with composer

```bash
composer require kalwa/kalwa-parser
```
    
## How to use?
 

```php

 try {
            $parser = new KalwaParser('MyCustomUserAgent');
            $parser->parse('https://themeselection.com/sitemap_index.xml');

            foreach ($parser->getSitemaps() as $url => $tags) {
             
                echo 'URL: ' . $url . '<br>';
             
                echo '<hr>';
            }
            foreach ($parser->getURLs() as $url => $tags) {
                echo $url . '<br>';  
            }
        } catch (SitemapParserException $e) {
            echo $e->getMessage();
        }

```
## Badges

kalwaParser

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)
[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![AGPL License](https://img.shields.io/badge/license-AGPL-blue.svg)](http://www.gnu.org/licenses/agpl-3.0)

