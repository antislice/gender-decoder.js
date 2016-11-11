# gender-decoder.js
A Javascript port of @lovedaybrooke's Python [gender-decoder](https://github.com/lovedaybrooke/gender-decoder). The original site is at [gender-decoder.katmatfield.com](http://gender-decoder.katmatfield.com/).

This script uses the original list of gender-coded words from the research paper written by Danielle Gaucher, Justin Friesen, and Aaron C. Kay: [Evidence That Gendered Wording in Job Advertisements Exists and Sustains Gender Inequality](http://gender-decoder.katmatfield.com/static/Gaucher-Friesen-Kay-JPSP-Gendered-Wording-in-Job-ads.pdf) (Journal of Personality and Social Psychology, July 2011, Vol 101(1), p109-28).

## Usage
Fancy packaging of this for Node is planned.

In the meantime, copy/paste the `gender-decoder.js` code into your own project. The `decodeGender()` function takes a String and returns this object:
```` javascript
{
  result: result, // "neutral", "strongly masculine-coded", "feminine-coded", etc
  explanation: explanation, // one sentence on what that means
  masculineCodedWords: masculineWords,  // list of masculine-coded words found
  feminineCodedWords: feminineWords   // list of feminine-coded words found
};
````

## Why?
Why port this? While working on [CodeForAmerica/posting-pro](https://github.com/codeforamerica/posting-pro), we wanted to have a more nuanced gender bias analysis than looking at pronouns.

Why do this analysis? A masculine sounding job posting will deter women from applying, while a feminine sounding job posting doesn't deter anyone. Obviously, neutral will be fine for everyone.
