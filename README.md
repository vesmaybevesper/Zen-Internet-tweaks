# Vesper's Zen Internet themes repository

Custom CSS for websites to make the internet beautiful. Transparency being the main feature, these themes also include removal of distractions and further useful features for each website.

![Screenshot](https://github.com/user-attachments/assets/a938e6b8-b120-4ba9-bc39-0ec932856dda)

## [How to get transparency in Zen](https://www.sameerasw.com/zen)

[![web-preview-zen](https://github.com/user-attachments/assets/dae63448-0fa8-44a7-a294-e18561de9389)](https://www.sameerasw.com/zen)

## Contributors

<a href="https://github.com/sameerasw/my-internet/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=sameerasw/my-internet" />
</a>

## Contributing styles

> ### Please make sure you go through all the provided instructions before submitting a new theme with a PR.

1. You can use the [example.com.css](https://github.com/sameerasw/my-internet/raw/refs/heads/main/websites/example.com.css) as a starter for most websites to grab the stylesheet format.
2. Make sure the file is named in the correct format [website domain].css (google.com.css and docs.google.com.css are 2 styles which are not merged unless you do 9.)
3. Please respect auto theming for day and night themes. If the website does not have a dark theme, account for dark reader.
4. Do not use wildcards such as applying transparency for all div elements since that is handled with force theming in the addon.
5. Every property should include `!important` to make sure it gets applied.
6. ~Do NOT leave commented out code.~ Now you can, but still DO NOT! But you can add descriptive comments... Check rule 15
7. Don't include `www` in the stylesheet file name.
8. Add proper comments for each section of a feature at the beginning with a clear but compact description.
9. For theming similar domains like app.arduino.cc , login.arduino.cc ..... similar urls with `prefixes`, you can add a general style with a leading `+` symbol when creating the stylesheet. ( `+arduino.cc.css` ) [example](https://github.com/sameerasw/my-internet/blob/main/websites/%2Bnixos.org.css)
10. Similarly, for theming websites with a shared domain but with different `suffixes` (like google.com, google.lk...), you can add the `-` symbol to the start of the stylesheet file name so it will replace the provided domain of the file name's domain. (`-google.com.css`). [example](https://github.com/sameerasw/my-internet/blob/main/websites/-ebay.com.css)
11. [optional] Each comment of the same file should have a unique domain specific identified prefix (yt- ytm- gh- ...) which will help the browser to separately apply themes.

    ```
      /* yt-transparency */
      :root{
        --colorBgApp: transparent !important;
      }

      /*  yt-no footer */
      footer.app-footer {
        display: none !important;
      }
    ```

12. Always make sure the first feature is `transparency` and also use the exact feature name without a difference allowing the global transparency toggle to work. Prefixes with `-` are acceptable.
13. Don't keep the firefox selectors if you are coying over from the userContent.css (remove `@-moz-document domain(" ")` )
14. Once comitted to the repository, github actions will parse the css file and update/ generate the [styles.json](https://github.com/sameerasw/my-internet/blob/main/styles.json) and then will be deployed to the github pages allowing the add-on to fetch from it.
15. _**[NEW!]**_ Now you can add descriptive comments to the css file which will be skipped during parsing and generating the styles.json file. BUT, make sure to start those css comment text with the `@` symbol as below examples. BUT, Any comment inside a feature in the css selectors or in properties will be skipped anyways.

    ```
      /* yt-transparency */
      /* @this comment will be skipped */
      :root{
        --colorBgApp: transparent !important;
        /* @ this comment will be skipped, but leaving it will cause no harm */
        /* This will be skipped */
      }

      /* @ this comment will be skipped */
      /*  yt-no footer */
      footer.app-footer, /* This will be skipped */
      footer {
        display: none !important;
      }
    ```

16. Website mapping. Use the `css-mapping.json` to map existing css styles to other websites. Also can be used for websites that works well with forcing.
17. You can add feature descriptions by separating the title and the rest of the text inside a feature comment by separating it with `$`. Check example.com.css for the samples.
    ```
      /* darkreader $ This is a example description */
      :root {
        --darkreader-background-ffffff: transparent !important;
      }
    ```
    This will show up like below while hovering the feature title.
    <img width="934" height="646" alt="CleanShot 2025-07-20 at 4  54 37@2x" src="https://github.com/user-attachments/assets/7bac8e98-c0d0-4c42-9c8b-b672fae65df8" />

>

### Thank you <3

<br>

<a href="https://star-history.com/#sameerasw/my-internet&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=sameerasw/my-internet&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=sameerasw/my-internet&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=sameerasw/my-internet&type=Date" />
 </picture>
</a>

[Browse the repository](https://github.com/sameerasw/my-internet)

[Visit my website](https://www.sameerasw.com)
