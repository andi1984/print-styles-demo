# Status Quo - Print styles and limitations

## Header and Footer

Best possible way seems to be to have an [absolute](https://stackoverflow.com/a/21043407/778340) (or fixed?) element on print mode?

Also interesting SO thread about headers [here](https://stackoverflow.com/questions/19646835/print-repeating-page-headers-in-chrome/25880258#25880258).

> I believe the correct answer is that HTML 5 and CSS3 have no support for printing page header and footers in print media.
>
> And while you might be able to simulate it with:
>
> - tables
> - fixed position blocks
>   they each have bugs that prevent them from being the ideal general solution.
>
>   -- [Ian Boyd, SO user](https://stackoverflow.com/a/7197225/778340)</cite>

And as an answer to this SO thread:

> The problem is browser vendors. You can make good-looking PDFs outside the browser using CSS Paged Media > with commercial tools like these (and there are others): Antenna House antennahouse.com/formatter, Prince princexml.com. – markg Sep 9 '19 at 1:28

### CSS Paged Media Module Level 3 Spec

In the [CSS Paged Media Module Level 3](https://drafts.csswg.org/css-page/) combined [CSS GCPM 3 spec](https://drafts.csswg.org/css-gcpm/) there is the possibility to define a DOM target that acts as a footer or header in the printed page.

There are tools like [PrinceXML](https://www.princexml.com/), [AntennaHouse](https://www.antennahouse.com/formatter-v7), [PDFReactor](https://www.pdfreactor.com/) or [WeasyPrint](https://weasyprint.org/) that support this spec!

A variety of tools can be compared and tested on [https://printcss.live/](https://printcss.live/).

An interesting article about possibilities can be found on [AListApart](https://alistapart.com/article/boom/).

Unfortunately there is no browser support yet:

- [Webkit](https://bugs.webkit.org/show_bug.cgi?id=15548)
- [Chromium](https://bugs.chromium.org/p/chromium/issues/detail?id=47277)

https://developer.mozilla.org/de/docs/Web/CSS/@page

## Table of contents

Cf. [w3.org](https://www.w3.org/Style/Examples/007/leaders.en.html)
