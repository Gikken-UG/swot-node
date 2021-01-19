# Swot :apple:
### :rotating_light: If you would like to add your school/educational institution, please create a pull request in [this repository](https://github.com/magicmarvman/swot-data). :rotating_light:

If you have a product or service and offer **academic discounts**, there's a good chance there's some manual component to the approval process. Perhaps `.edu` email addresses are automatically approved because, for the most part at least, they're associated with American post-secondary educational institutions. Perhaps `.ac.uk` email addresses are automatically approved because they're guaranteed to belong to British universities and colleges. Unfortunately, not every country has an education-specific TLD (Top Level Domain) and plenty of schools use `.com` or `.net`.

Swot is a community-driven or crowdsourced library for verifying that domain names and email addresses are tied to a legitimate university of college - more specifically, an academic institution providing higher education in tertiary, quaternary or any other kind of post-secondary education in any country in the world.

If you would like to add your school/educational institution, please create a pull request in [this repository](https://github.com/magicmarvman/swot-data).

### Installation

Add `swot-node` like other NPM packages, simply run:

`yarn add swot-node`

or

`npm install swot-node`

### Usage

#### Verify Email Addresses

```javascript
const swot = require("swot-node")

swot.isAcademic('lreilly@stanford.edu')           // true
swot.isAcademic('lreilly@strath.ac.uk')           // true
swot.isAcademic('lreilly@soft-eng.strath.ac.uk')  // true
swot.isAcademic('pedro@ugr.es')                   // true
swot.isAcademic('lee@uottawa.ca')                 // true
swot.isAcademic('lee@leerilly.net')               // false
```

#### Verify Domain Names

```javascript
const swot = require("swot-node")

swot.isAcademic('harvard.edu')              // true
swot.isAcademic('www.harvard.edu')          // true
swot.isAcademic('http://www.harvard.edu')   // true
swot.isAcademic('http://www.github.com')    // false
swot.isAcademic('http://www.rangers.co.uk') // false
```

#### Find School Names

```javascript
const swot = require("swot-node")

swot.getSchoolName('lreilly@cs.strath.ac.uk')
// => "University of Strathclyde"

swot.getSchoolName('http://www.stanford.edu')
// => "Stanford University"
```

### See Also

* [swot](https://github.com/leereilly/swot) - original ruby version of swot
* [gman](https://github.com/benbalter/gman) - like swot, but for government emails
* [swotphp](https://github.com/mdwheele/swotphp) - PHP port of Swot
* [swot-simple](https://github.com/mapbox/swot-simple) - JS port of Swot
* [swot-clj](https://github.com/ipavl/swot-clj) - Clojure port of Swot
* [swot](https://github.com/abadojack/swot) - Go port of Swot
