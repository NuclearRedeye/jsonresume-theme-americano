# Americano Theme

Americano is a [JSON Resume](https://jsonresume.org/) theme based on the [Macchiato Theme](https://github.com/biosan/jsonresume-theme-macchiato).

## Quick Start

1. Download [JSON Resume CLI](https://jsonresume.org/)
  ```
  npm install -g resume-cli
  ```

2. Download the theme from [npm](https://www.npmjs.com/)
  ```
  npm install -g jsonresume-theme-macchiato
  ```

3. Use resume cli to build your resume
  ```
  resume export resume.html --theme macchiato
  ```

### PDF output

Probably you want a PDF version of your resume...

JSONResume CLI should be able to make a PDF out of your JSON but I always struggled to get it to work,
so I switched to a more direct and effective approach.

I use Puppeteer-CLI to make a PDF from my HTML resume.

```
npm install -g puppeteer-cli
puppeteer --wait-until networkidle0 --margin-top 0 --margin-right 0 --margin-bottom 0 --margin-left 0 --format A4 print resume.html resume.pdf
```

Obviously you could write a very simple Node script to use the real Puppeteer and the `render` function to make a PDF without first exporting the HTML version.

Also checkout [HackMyResume](https://github.com/hacksalot/HackMyResume), a powerful tool to build and analyze your JSON Resume.


## License

Available under the [MIT license](http://mths.be/mit).

