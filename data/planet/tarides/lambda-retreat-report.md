---
title: Lambda Retreat Report
description: "Today we're taking a little pause from our OCaml 5 series to talk about
  a programming retreat. I spent a week in the woods with fellow\u2026"
url: https://tarides.com/blog/2023-01-12-lambda-retreat-report
date: 2023-01-12T00:00:00-00:00
preview_image: https://tarides.com/static/9f22d11ae4e2bed027c4f8669055f956/0132d/lambda.jpg
featured:
---

<p>Today we're taking a little pause from our OCaml 5 series to talk about a programming retreat. I spent a week in the woods with fellow programmers at the <a href="https://anandology.com/lambda-retreat/">Lambda Retreat</a>. It was a wonderful way to explore the nature of computations, abrstractions, and paradigms. Although I mostly work in OCaml, it was fun and challenging to code in Scheme, another functional programming language.</p>
<p>For more OCaml 5 posts, visit our <a href="https://tarides.com/blog">Tarides blog</a> for posts about some exciting new features and interviews with OCaml programmers, <a href="https://tarides.com/blog/2023-01-10-engineer-spotlight-sudha-parimala">including one with me</a>! Next week, come back to read an article about how OCaml 5 performs during the <a href="https://benchmarksgame-team.pages.debian.net/benchmarksgame/index.html">Benchmarking Game</a>, but for now, read on for a Lambda Retreat Retrospective.</p>
<hr/>
<p><em>Structure and Interpretation of Computer Programs (SICP)</em> is many programmers' favourite programming textbook. It teaches programming constructs like recursion, modularity, abstractions, etc. For a long time, it was used as the textbook for an introduction to programming course. Here's what <a href="https://www.amazon.com/review/R403HR4VL71K8">Peter Norvig</a> and <a href="https://eli.thegreenplace.net/2008/05/28/book-review-structure-and-interpretation-of-computer-programs-by-harold-abelson-gerald-jay-sussman/">Eli Bendersky</a> have to say about SICP.</p>
<p>Having seen a lot of people highly recommend SICP, I grabbed a copy for myself a few years ago and started reading it, but, alas, I never completed the book.</p>
<p>In the latter part of last year, <a href="https://anandology.com/">Anand</a> decided to host a week-long retreat to gather a bunch of people and go through some interesting parts of SICP. Suffice it to say, I jumped at the opportunity to do nothing but read and write code for a week.</p>
<h3 style="position:relative;"><a href="https://tarides.com/feed.xml#getting-ready" aria-label="getting ready permalink" class="anchor before"><svg aria-hidden="true" focusable="false" height="16" version="1.1" viewbox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Getting Ready</h3>
<p>Two weeks before the retreat, we had some warm-up sessions to get ourselves ready. During this time, we attended some remote sessions and solved a few exercises from the Chapters 1 &amp; 2 of SICP.</p>
<h3 style="position:relative;"><a href="https://tarides.com/feed.xml#arriving" aria-label="arriving permalink" class="anchor before"><svg aria-hidden="true" focusable="false" height="16" version="1.1" viewbox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Arriving</h3>
<p>On Day 0, we all arrived at Bangalore from various parts of India, and carpooled to the <a href="https://tvc.farm/">Tamarind Valley Collective</a> (TVC), located ~80km from the city. Reaching TVC turned out to be an unexpected but enjoyable 1.5km trek, since the roads to the campsite were unusable due to rain.</p>
<h3 style="position:relative;"><a href="https://tarides.com/feed.xml#at-the-retreat" aria-label="at the retreat permalink" class="anchor before"><svg aria-hidden="true" focusable="false" height="16" version="1.1" viewbox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>At the Retreat</h3>
<p><strong>Functional Geometry</strong></p>
<p>The retreat began with Functional Geometry from the second chapter of SICP. We started with the basics, like rendering images, and slowly built the primitives needed for generating Escher's woodcut.</p>
<p>It was amazing to see the power of composability! We thoroughly enjoyed building Escher's woodcut from an unassuming image of a fish.</p>
<p><span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 305px; ">
      <a href="https://tarides.com/static/91ad732ce9c8ddafb7f72036ecd368e1/a3e09/fish.png" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 80.58823529411765%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAQCAYAAAAWGF8bAAAACXBIWXMAAAsTAAALEwEAmpwYAAACGklEQVQ4y5VU2YriUBD1/7/AV8EVwQcRG23BfcO1dQTXMXFG7RizaWI0as5QtyeijkpPQUHlUnXuqTqV61pLBrb6AZJsgJ8pWK0NmOYemqZCUVUIyicmP6fo/ehgNJ7gUxAwHAwwmoyx0tbYGTvohg7DMJi7NOMI42BD2RywXJuQNAumeYBlHaDrOkRFwOzXbwwHfUw5DtpmgxnPg5vxkLcKTNPEbre7uAuqiLO0gi2LwJIDVAl7Q0elWmU3fpkNx87n8yW2T2ecTqcbd500Bce1iKO0hrVa4qjIwOkISZZRr9ex3W5xbQRo2zbzR+a6P3DSFosF3t/fkUwmoaoq9vs9LMv6yvkL+Mhd9wdOS+FwGB6PB9lsFolEAo1GA6VSCZVK5Qb0JcPrpFgshkKhwOJqtYper4ePjw8Eg8HvA94njsdjTKdT1j6Btdtt+P3+/2NIRmo57efzeTZDmifP84jH408FeQpI+9dqtVjc6XRQLpcxHA7R7/eZ8vfCfGuGoVAIuVyOxSQGiZPJZBhLURRvVui69iFDSiQ13W433t7eMJlMEI1GmdrkgiD8s5tO/dMZUqskQjqdRiAQYIoTOKns8/kY21qtdgGnmpct05oQSLfbZd9UmEql2EU0y2KxyGJiLMvya4bUAgnhCOC0RH+Ks+TNZhORSIQx9nq9FxEfAlLhaDS6Ob9+FDiOw3w+Z+IQc+qCQGm9/gBmY7Y17ro+DwAAAABJRU5ErkJggg=='); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/91ad732ce9c8ddafb7f72036ecd368e1/a3e09/fish.png" class="gatsby-resp-image-image" alt="fish" title="fish" srcset="/static/91ad732ce9c8ddafb7f72036ecd368e1/04472/fish.png 170w,
/static/91ad732ce9c8ddafb7f72036ecd368e1/a3e09/fish.png 305w" sizes="(max-width: 305px) 100vw, 305px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span></p>
<p align="center">
  <span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 514px; ">
      <a href="https://tarides.com/static/ae748b6f80360897b268809e102ce128/dea13/woodcut.png" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 94.70588235294117%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAATCAYAAACQjC21AAAACXBIWXMAAAsTAAALEwEAmpwYAAACPElEQVQ4y61UZ48aQQzl//8NJHrvvemOi6hLOYoQ5ANKFALLdkA0R89o9k53gfuQrGSN7fE8P9uz4zBNkzRNswW2ZVlkGAbruq7zut/v2Q+BT1VV9iNO0zVSVIX9jsPhwJsQXVdJkrr08vKNSqUSdbsSWZZJr68Denp6pkajwTKfz2k2m1G1WqXhcEg/Vz/o+68JyZvfN0CRyTQN2m63tF6vabVasQ5GsizTcrlk32azYSaKotxi5C3phkaaofB5x/V6Jci/fDeM2+qA43K50GKxoPF4TJPJxBbY0+mU9dFoZOsQ6LvdzgYUHwOeTifKZDLkdDopkUhQOBwmr9dLqVSKXC4XBYNBisfjrCeTSbb9fj+X/8bw+sYQgJVKhbLZLOXzeXvN5XJUKBSoVquxjqSwsQ9g9PYuw3K5zEHpdJoPIQGmWCwWWcAWMahA2BjaXwHP5zNfE5QBEJTs8XiYGVi1Wi32ud1u3o9GoyxfMkSZYAgWzWaTbTDBvUPJ9XqdEwv/Q0AEggHY4IAkSXyJAY7DkUiE/SIphvSwZDCMxWLcP7BBPwEEADAbDAast9ttjoPcZXg8HhkQ04OgXID2+30eDoDBGHvQUc2XU0aQz+ezm47yO50OA2MPjMSgBMO7JYuhvL9/ENgAgCCR2Iegtw8ZojQ0WgCJewd2GAJ8uELQRY8fMkQQfi0cwK8VCoU4AUrHYbQB9xSJsB8IBO4zxOOAn73X6/H7holiIFhhC9/HPTxtnwD/x9P1/vsDiUZKxiVGtrgAAAAASUVORK5CYII='); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/ae748b6f80360897b268809e102ce128/dea13/woodcut.png" class="gatsby-resp-image-image" alt="Escher's Woodcut" title="Escher's Woodcut" srcset="/static/ae748b6f80360897b268809e102ce128/04472/woodcut.png 170w,
/static/ae748b6f80360897b268809e102ce128/9f933/woodcut.png 340w,
/static/ae748b6f80360897b268809e102ce128/dea13/woodcut.png 514w" sizes="(max-width: 514px) 100vw, 514px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span>
&nbsp; &nbsp; &nbsp; &nbsp;
  <span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 680px; ">
      <a href="https://tarides.com/static/35f581f60f5317fa1f360d000beff8b5/37523/group2.png" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 56.470588235294116%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAALCAIAAADwazoUAAAACXBIWXMAAAsTAAALEwEAmpwYAAACoklEQVQozwXBC08SAQAA4PsdbjU05CEIocQUxYUPNOVxHMhLuIMDjqeGBHF3gMgJ8QhygqKmqSN85cwZ2KgVa8xmbupWv6jvAzg0OuNRZ1dHJ7uzW9jDGeDyhUyekM23WPSFNcvRMVyruc4/+2uHrno9eNUkfrVT//6SjSvD0ScdMNLLnOhjjQvYIlb3AKt7gMvq5/YM8Xn9DPawSFAqIa128Ob361YrdHtH3jwQt/fk/Z2vfY00flgAcJCjEXXrh3pkQtbUIFcrF8nlYtm4WDrYq5AKkLmR6pn58hta/+5ptkKtduj4wvylaWy37ZdfUSBPqXC3JIRJpqd4HR2Pn9AYXTQGjyvoYTLXMtD+pqr2Ub1VMWQi6O6uvd7wnjecD3f+P9fk2UUQIGLavYr1dN+jg8QMOp3PYcvUHst8FjSHYIcDCwdy5QxVXF+IVbMb2a2DVycnsasm1WovVw5dQC6gD9uVb4I6H6Iak0qHxWKlbn4+to24U0o4OmbPL6ZO3dGDQP4nTlLxt2R+O5XdSmZ2cLLgBXx6BTgqVkn6oOlRaFarBZUe1J6ILkEKQzixIxqDjbawSg0znilhjTFXSBQ/5JIZciWbSKYTgNVqNUEv9JpZhcE0DWrVk+NexOS0WugswVMxOCRVO50Bo8FKYw+ZZhTFVLy0uZbI4pFkaCkZBxAbNjE5o0FJ20LcijoX3U6v02/Sm9hsQW/f5EvMm8aJgHdRJtP6jXrK66CSeK6yUtjN5TbSgBHxjUufy+UQ5nA7zDA8a/BbsehCENXoKDx+UinvZqjVGJEhIvnQAuV34Jg5vRzaq5a2q++ARSI1j8HRSMRmgUeGJSgIYpCadGHlROx85/1haXUjubS2FCsvx0txgsAQ35wm6rFvlzPrleJ/WlYUa5KVSTEAAAAASUVORK5CYII='); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/35f581f60f5317fa1f360d000beff8b5/c5bb3/group2.png" class="gatsby-resp-image-image" alt="Participants with Lambda Retreat t-shirt" title="Participants with Lambda Retreat t-shirt" srcset="/static/35f581f60f5317fa1f360d000beff8b5/04472/group2.png 170w,
/static/35f581f60f5317fa1f360d000beff8b5/9f933/group2.png 340w,
/static/35f581f60f5317fa1f360d000beff8b5/c5bb3/group2.png 680w,
/static/35f581f60f5317fa1f360d000beff8b5/37523/group2.png 720w" sizes="(max-width: 680px) 100vw, 680px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span>
</p>
<p>Anand rewarded everyone with an Escher's woodcut T-Shirt for successfully generating the <code>square-limit</code> \o/</p>
<p>We then abstracted out the implementation details for the Functional Geometry primitives we had built. The abstraction gives us the freedom to change the implementation at a later point without affecting the higher-level details.</p>
<p><strong>Mutability and State</strong></p>
<p>We spent some time understanding mutations, global state, and local state in Scheme, a functional language like OCaml. This led us to building some mutable data structures, like a mutable queue and a mutable hash table in Scheme, and generalising with a dispatcher to perform operations.</p>
<p><strong>Metacircular Interpreter</strong></p>
<p>Another exercise before the retreat was to write a parser for Scheme in Python. At the retreat, we started with translating it to Scheme. Going further, we built a metacircular interpreter -- a Scheme interpreter written in Scheme. How cool is that?</p>
<p>We then learnt about lazy evaluation in Scheme and went on to make our metacircular interpreter lazy by default. Another interesting part we looked forward to was targeting WebAssembly (Wasm) from Scheme. It was surprisingly simple to go from Scheme to Wasm, targeting Wasm's Lisp-like syntax.</p>
<h3 style="position:relative;"><a href="https://tarides.com/feed.xml#beyond-tech" aria-label="beyond tech permalink" class="anchor before"><svg aria-hidden="true" focusable="false" height="16" version="1.1" viewbox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Beyond Tech</h3>
<p>Living at TVC in the middle of a forest with barely any electricity or cellular network for a week was a humbling experience. Madhav, the resident manager at TVC, and his team made sure our stay was comfortable. The food, made from locally-sourced indgredients featuring local cuising was amazing!</p>
<p><span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 680px; ">
      <a href="https://tarides.com/static/23dba1a715848b57cf73cb75d4404490/eea4a/campsite.jpg" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 75.29411764705883%; position: relative; bottom: 0; left: 0; background-image: url('data:image/jpeg;base64,/9j/2wBDABALDA4MChAODQ4SERATGCgaGBYWGDEjJR0oOjM9PDkzODdASFxOQERXRTc4UG1RV19iZ2hnPk1xeXBkeFxlZ2P/2wBDARESEhgVGC8aGi9jQjhCY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2P/wgARCAAPABQDASIAAhEBAxEB/8QAGAAAAwEBAAAAAAAAAAAAAAAAAAIEAwX/xAAVAQEBAAAAAAAAAAAAAAAAAAAAAv/aAAwDAQACEAMQAAABqTnNDYlD/8QAGhAAAgMBAQAAAAAAAAAAAAAAAAECAxEEEv/aAAgBAQABBQJdMWWXRzSK0bSPZ//EABURAQEAAAAAAAAAAAAAAAAAABAR/9oACAEDAQE/AYf/xAAWEQEBAQAAAAAAAAAAAAAAAAAAEgH/2gAIAQIBAT8BpWv/xAAYEAACAwAAAAAAAAAAAAAAAAAAEAIRIf/aAAgBAQAGPwJZIp//xAAcEAACAgIDAAAAAAAAAAAAAAAAAREhUWExcZH/2gAIAQEAAT8h5JxjY7JS+i9waFtZoqkvR2wf/9oADAMBAAIAAwAAABCPD//EABQRAQAAAAAAAAAAAAAAAAAAABD/2gAIAQMBAT8QH//EABcRAAMBAAAAAAAAAAAAAAAAAAABUWH/2gAIAQIBAT8QbwwP/8QAHBABAQEAAQUAAAAAAAAAAAAAAREAMSFBUWHR/9oACAEBAAE/EG1YWJaYMgeAfc8JKWu2hgrUGYU4RF6rpqh6S7//2Q=='); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/23dba1a715848b57cf73cb75d4404490/7bf67/campsite.jpg" class="gatsby-resp-image-image" alt="campsite" title="campsite" srcset="/static/23dba1a715848b57cf73cb75d4404490/651be/campsite.jpg 170w,
/static/23dba1a715848b57cf73cb75d4404490/d30a3/campsite.jpg 340w,
/static/23dba1a715848b57cf73cb75d4404490/7bf67/campsite.jpg 680w,
/static/23dba1a715848b57cf73cb75d4404490/990cb/campsite.jpg 1020w,
/static/23dba1a715848b57cf73cb75d4404490/eea4a/campsite.jpg 1280w" sizes="(max-width: 680px) 100vw, 680px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span></p>
<p>The evening walks and hikes at TVC were memorable. We managed to sight some kingfishers and owls while snacking on some freshly plucked tamarinds. We had so much fun hiking along a stream that runs in the middle of TVC and capturing wisdom about sustainable living from Madhav and Vikrant, who put it into practice by living on farms.</p>
<p align="center">
  <span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 447px; ">
      <a href="https://tarides.com/static/8091856d2296477e493c94038c366f82/a2d48/owl.png" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 76.47058823529412%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAPCAYAAADkmO9VAAAACXBIWXMAAAsTAAALEwEAmpwYAAADaklEQVQ4y3WP209jVRSHz59lvIyJSDpQaCntAC0MbYWhQGspbc+hPe1pe3q/cBnBmPgyGuNoMgmjUTOD0EILTMlkwERf1BcffPLJRGNoTy9+pmWGxDg+fNl7Za/1W98WvI8u8T5qsNLnEt/jS1b3LvF/23gpL97EsoZS04hWr4hUNUKHGsJqv+nfAy/4/7AW8lEL5XmYfKQRqmisVVoIwQONwH7zmpdZBfYbBPrnJeJBA6nc7Ntc9TcJ7muIB1cIcq1DuNpGqrT63wiWtf8E9+re9nCtg1xrE+4ZHbauJaSyhli+uguR4w59Trp95ONuf1CqtFk77CAdtgnuNxErbaTHfyDu/dVf3jP07TX6AokTjUhNQ642EcK1LqFqC7nWInLcviZ60iF20iFR7xA9/Zts9Xe2ckn8yR2U0y7Zukaux1mbzYsOqXqLwtM2QvioiXwK4R51kJ8TqUOsDuqTNkodNiu/cr8UoBh2U3jwhPd+gO1zjdKzNpmzDtsXHXa+6yCE0utI+feJ7HyG8vEe0fsnxL/6GfXgN9Tqn6hnXeJPIXXWpfz1J3y5HUT2LqI8/JHUBcROGqTrbTaetdk8byE4nHNIfi8xWSS65kMJ+YnLQTaLSfKlIoWdD8l/tEvy8yc82P2ULz4QCSzZMVpsyA9/Ivs9pM8heQHZCxCc7gAubwBJjpLKZlDiMRRFplRIUkhHyCck7mZDbKZECqkwxaxMLq2wFvSg5kuo974hdK+MuntO8eAXBJvNiX3WhWtuEa/Hg3/VT0BaI5tLks2nyObSlNYz5AsqG6UkG8Uk2Uyc9fU0xXyChOzHuzSPGg2QUGSEwVcHmDdZcejNjL4+wIxuFJ/NgThhxTtpJbC4hOJ2IzrtKGKAdCZBQo2ytZVj626RmBpHDEnk82kyGRVh2TyDZ9zGgt7M3JAJ96gF/9gk7uExbG8OMvbaAPM3DYy+cgO73oi6vISysEDE7SYvS6TFVUTPMslYhHwqjuAaNmF8YxDjDR0+ywxBsw2nzsCszoDTeItlqwPP5Cwui5VF8xReyzT+qds4bo5gf3sI2TLBu8MjrJgniTveQXCNjDM9ZMT41hBLxglWTJPc0Y9jGxxmVm/CbbHiGDIwrRvFM3Eb39QsToOZKZ0ex8g4dwy3sOtGmNObCJqt/AN9gDnmEwfOegAAAABJRU5ErkJggg=='); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/8091856d2296477e493c94038c366f82/a2d48/owl.png" class="gatsby-resp-image-image" alt="An owl we spotted" title="An owl we spotted" srcset="/static/8091856d2296477e493c94038c366f82/04472/owl.png 170w,
/static/8091856d2296477e493c94038c366f82/9f933/owl.png 340w,
/static/8091856d2296477e493c94038c366f82/a2d48/owl.png 447w" sizes="(max-width: 447px) 100vw, 447px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span>
&nbsp; &nbsp; &nbsp; &nbsp;
  <span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 680px; ">
      <a href="https://tarides.com/static/1a6b3dd1fda189aabdd21e1591229a8d/eea4a/group.jpg" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 75.29411764705883%; position: relative; bottom: 0; left: 0; background-image: url('data:image/jpeg;base64,/9j/2wBDABALDA4MChAODQ4SERATGCgaGBYWGDEjJR0oOjM9PDkzODdASFxOQERXRTc4UG1RV19iZ2hnPk1xeXBkeFxlZ2P/2wBDARESEhgVGC8aGi9jQjhCY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2P/wgARCAAPABQDASIAAhEBAxEB/8QAFwABAQEBAAAAAAAAAAAAAAAAAAMBBP/EABYBAQEBAAAAAAAAAAAAAAAAAAEAAv/aAAwDAQACEAMQAAAB1OGXqEf/xAAcEAEAAgEFAAAAAAAAAAAAAAABAAIRAxITISL/2gAIAQEAAQUCrqI8nTZz5Y2ZuMf/xAAUEQEAAAAAAAAAAAAAAAAAAAAQ/9oACAEDAQE/AT//xAAVEQEBAAAAAAAAAAAAAAAAAAAAEf/aAAgBAgEBPwFH/8QAGRAAAgMBAAAAAAAAAAAAAAAAACEBAhAR/9oACAEBAAY/Ah5NuPHB/8QAHBAAAwACAwEAAAAAAAAAAAAAAAERMUEhcYGR/9oACAEBAAE/IavEVNTNV/BDb0XHYIhFVNdCgpT/2gAMAwEAAgADAAAAEEc//8QAFhEBAQEAAAAAAAAAAAAAAAAAAAER/9oACAEDAQE/EK1//8QAFhEAAwAAAAAAAAAAAAAAAAAAAAER/9oACAECAQE/EFGQf//EABwQAQACAgMBAAAAAAAAAAAAAAERIQBBMVFhcf/aAAgBAQABPxB5FFibvGlYZvl1jAJnfLEFHkag39xi+EWPXCq5koJXmf/Z'); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/1a6b3dd1fda189aabdd21e1591229a8d/7bf67/group.jpg" class="gatsby-resp-image-image" alt="After a hike along the stream" title="After a hike along the stream" srcset="/static/1a6b3dd1fda189aabdd21e1591229a8d/651be/group.jpg 170w,
/static/1a6b3dd1fda189aabdd21e1591229a8d/d30a3/group.jpg 340w,
/static/1a6b3dd1fda189aabdd21e1591229a8d/7bf67/group.jpg 680w,
/static/1a6b3dd1fda189aabdd21e1591229a8d/990cb/group.jpg 1020w,
/static/1a6b3dd1fda189aabdd21e1591229a8d/eea4a/group.jpg 1280w" sizes="(max-width: 680px) 100vw, 680px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span>
</p>
<p>Our coworkers Pappu the hunting cat, her three kittens, and our boy Poco, the rugged looking sweet doggo, kept us company.</p>
<p align="center">
  <span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 537px; ">
      <a href="https://tarides.com/static/ab433e19fe4942a338efd9f13e1adf60/b1cde/cat.png" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 77.64705882352942%; position: relative; bottom: 0; left: 0; background-image: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABQAAAAQCAYAAAAWGF8bAAAACXBIWXMAAAsTAAALEwEAmpwYAAAEXElEQVQ4ywXB6U+TBwDA4feLH7a4ZVPcCB7MA1AEMxSFQkUQWEtBhBYoIPTtZUct5Si0BQqlBy3lKGdFxIjzAltRHOJQwGOJC87pNDPZviz7V357HuHuywkWN6+wtD5NdPMO0Xcf6ZuK4J0d5v7vARY3zDx6rWPlrZlnn5zcf+nF1mtm4vEckzMR+hw2RkMhbkV/JnL1BsLsspmZqJabsTZuLnm4vT5LV8CGf66bxdd2YlsmYr/pWdwSefK3husrjYRnRVb/7GdsYhifq5vI1CT3Hq4xHYkgTExfZGRKZGRGz/RCO+HFNvSWUtzjJiIPWnGF6hhdrGXg1nnCsTLsAwpcfjnRZybGh/sZdjsZDgYYCATxBzwIK7FeVn/pZe1XH6svJ3j0JkBHTzU6UzWqC3IuiVX4Ao1Mr4lcXpXR0VOCPSxj9LKea34bU34nY+Ewk5MzTF5zIDx95eH5Voi5eS+dnTZaO02cOJXJrri9xMXtxmQUEasrqW84h75ZQf0FOb1BNdE5J/eG7MyNj3J3cYnNZxuMOkWEm9FebkX7aDJryMmRkHQ4jfiERFJSktm9Zx+qynLaLDoKzuQhK5ZhMdZy2dvK3WA7kb4WhvxuBoMj+F3dGEtzEIrz8yg5k4mmsZac7OOcyjhCRloK+/ft5Ysvd5JzKpMKRT4ajZrREQ/jPisL0x3cGWyisaqKIkkGJ5IS+Tb+APu+3o7QpFbQLVbQ0tJMnUpBUc4xMo+lcDTpAIf27yf9cBJJ3yUwFPIxcyWM/IdsIm4ds4NWVKpaMtKPk374KKlpJ4jfsQuhs7UZo/4iKrWeSyYtivyT1CrlqCuKqS4vQqMup1J+lvnIGI8fP8DX28xGdITl2DXUNSIKuZKzBTKk2bmkHk5HMBqsWMx2WpqdOB1OtA1K2ix6OqwGzLoa/O4OWg0iAYuJDx/e8GLzIR/frbOyHMNiaudHoxW91oK2To+qsh7BaulEJ5oR6/ScKy2ntKQYh72VDqsek0ZFV5uRZkMtjmYjsXvXebp2n78+vmJp4Q6dVic9jn7GBqfwuUfo6xpAaLF0oBXNVKsu8H1GFju+2klycgpiXSVN2mrsLQbGh1wMelr46WqI93+84L9/3xK7Pc9of4iQN4S3Z4AhzxAD/YMIWo0Jk86EulJNbtZpvolLYNu2z0hPO4qxsQqztpqJoW4WbgTZWL3OP5+e82ZrHY/LQ8jlIewZxNHhJuwdJRwII8hk5RTkFZMryUcqkZJyKJX4XQls/+xzEvckUFNehN2qZX52gLdbT3j//jnLt28w2OPBZXcx6Qvh6fbS7/QSCY0jlCkqqFHWkZVTiFSST4HkNEeSUzmYeJA98QkcOpjEmexs6pUVGA06FPIStFVV2Jqa0YgmbFY7nm4fDlsP7W1dCJo6HQ1qkfIyJQpZGbnSQqTZeZQWliDJkiI5mUuh9Cz5uQUoS89TXCinQVlFu96MQWvAbm4l2OVmpC+IpyfI/1Z52cmsSVniAAAAAElFTkSuQmCC'); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/ab433e19fe4942a338efd9f13e1adf60/b1cde/cat.png" class="gatsby-resp-image-image" alt="Pappu the cat" title="Pappu the cat" srcset="/static/ab433e19fe4942a338efd9f13e1adf60/04472/cat.png 170w,
/static/ab433e19fe4942a338efd9f13e1adf60/9f933/cat.png 340w,
/static/ab433e19fe4942a338efd9f13e1adf60/b1cde/cat.png 537w" sizes="(max-width: 537px) 100vw, 537px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span>
&nbsp; &nbsp; &nbsp; &nbsp;
  <span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 680px; ">
      <a href="https://tarides.com/static/2c0f98a83217cb6e933920968f817edf/eea4a/poco-dog.jpg" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 75.29411764705883%; position: relative; bottom: 0; left: 0; background-image: url('data:image/jpeg;base64,/9j/2wBDABALDA4MChAODQ4SERATGCgaGBYWGDEjJR0oOjM9PDkzODdASFxOQERXRTc4UG1RV19iZ2hnPk1xeXBkeFxlZ2P/2wBDARESEhgVGC8aGi9jQjhCY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2P/wgARCAAPABQDASIAAhEBAxEB/8QAGAAAAwEBAAAAAAAAAAAAAAAAAAIFAwT/xAAWAQEBAQAAAAAAAAAAAAAAAAACAAH/2gAMAwEAAhADEAAAAV14ENWJJp//xAAbEAACAQUAAAAAAAAAAAAAAAAAARMQERQhMv/aAAgBAQABBQKZsn1mFjmn/8QAFBEBAAAAAAAAAAAAAAAAAAAAEP/aAAgBAwEBPwE//8QAFhEAAwAAAAAAAAAAAAAAAAAAAQIQ/9oACAECAQE/AQs//8QAGxAAAQQDAAAAAAAAAAAAAAAAEQABAhASITH/2gAIAQEABj8CyKLMZFcrVf/EABsQAAMAAgMAAAAAAAAAAAAAAAABESGhMUHw/9oACAEBAAE/IaKqPhmaauSL7llR5cY6mwvZP//aAAwDAQACAAMAAAAQG/8A/8QAFhEBAQEAAAAAAAAAAAAAAAAAACFB/9oACAEDAQE/EMV//8QAFhEBAQEAAAAAAAAAAAAAAAAAAREQ/9oACAECAQE/EAtc/8QAHhABAAICAQUAAAAAAAAAAAAAAQARMUFRYXGhweH/2gAIAQEAAT8QNuwYvkDeRRtXiViDHcgLImTuAYiXAzbx7iawvWP/2Q=='); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/2c0f98a83217cb6e933920968f817edf/7bf67/poco-dog.jpg" class="gatsby-resp-image-image" alt="Hiking crew with Poco the dog" title="Hiking crew with Poco the dog" srcset="/static/2c0f98a83217cb6e933920968f817edf/651be/poco-dog.jpg 170w,
/static/2c0f98a83217cb6e933920968f817edf/d30a3/poco-dog.jpg 340w,
/static/2c0f98a83217cb6e933920968f817edf/7bf67/poco-dog.jpg 680w,
/static/2c0f98a83217cb6e933920968f817edf/990cb/poco-dog.jpg 1020w,
/static/2c0f98a83217cb6e933920968f817edf/eea4a/poco-dog.jpg 1280w" sizes="(max-width: 680px) 100vw, 680px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span>
</p>
<p>Our days of hacking were followed by board games in evenings and nights. We had so much fun and laughter riots playing games like Skull, Chameleon, and Ticket to Ride Europe. By the end of the retreat, we were surprised by how little internet and social media we had consumed that week!</p>
<p><span class="gatsby-resp-image-wrapper" style="position: relative; display: block; margin-left: auto; margin-right: auto; max-width: 680px; ">
      <a href="https://tarides.com/static/f0ce14e49dabc260374548b09e1b66c9/dc896/game.jpg" class="gatsby-resp-image-link" style="display: block" target="_blank" rel="noopener">
    <span class="gatsby-resp-image-background-image" style="padding-bottom: 119.41176470588235%; position: relative; bottom: 0; left: 0; background-image: url('data:image/jpeg;base64,/9j/2wBDABALDA4MChAODQ4SERATGCgaGBYWGDEjJR0oOjM9PDkzODdASFxOQERXRTc4UG1RV19iZ2hnPk1xeXBkeFxlZ2P/2wBDARESEhgVGC8aGi9jQjhCY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2NjY2P/wgARCAAYABQDASIAAhEBAxEB/8QAFwABAQEBAAAAAAAAAAAAAAAAAAQDAf/EABYBAQEBAAAAAAAAAAAAAAAAAAEAAv/aAAwDAQACEAMQAAABj5doUjrZvqZYgX//xAAcEAACAwADAQAAAAAAAAAAAAABAgADEwQSISL/2gAIAQEAAQUCy7TDzFDKPoFYwZDxyoqa2uapP//EABQRAQAAAAAAAAAAAAAAAAAAACD/2gAIAQMBAT8BH//EABYRAAMAAAAAAAAAAAAAAAAAAAAQEf/aAAgBAgEBPwFw/8QAHBAAAgICAwAAAAAAAAAAAAAAAAECERAhMTJB/9oACAEBAAY/AtHhcYjlWKg9Cto7I5P/xAAcEAADAAIDAQAAAAAAAAAAAAAAAREhMUFRYYH/2gAIAQEAAT8ha4ysXY+TToS0DQvykM3j2NsWxJtcyi95PR0P/9oADAMBAAIAAwAAABAU2AH/xAAWEQADAAAAAAAAAAAAAAAAAAAAEBH/2gAIAQMBAT8QdP/EABoRAAAHAAAAAAAAAAAAAAAAAAABEBEhQVH/2gAIAQIBAT8QxxJUr//EABwQAQADAAMBAQAAAAAAAAAAAAEAESFBUWEx8P/aAAgBAQABPxC1ydNW3Wrx9g0tbgnvchtFO3HqYSoot4CJUsCrz6QIK/Du/iKCqUic8wEW0qtQ6q/tz//Z'); background-size: cover; display: block;"></span>
  <img src="https://tarides.com/static/f0ce14e49dabc260374548b09e1b66c9/7bf67/game.jpg" class="gatsby-resp-image-image" alt="game" title="game" srcset="/static/f0ce14e49dabc260374548b09e1b66c9/651be/game.jpg 170w,
/static/f0ce14e49dabc260374548b09e1b66c9/d30a3/game.jpg 340w,
/static/f0ce14e49dabc260374548b09e1b66c9/7bf67/game.jpg 680w,
/static/f0ce14e49dabc260374548b09e1b66c9/990cb/game.jpg 1020w,
/static/f0ce14e49dabc260374548b09e1b66c9/dc896/game.jpg 1294w" sizes="(max-width: 680px) 100vw, 680px" style="width:100%;height:100%;margin:0;vertical-align:middle;position:absolute;top:0;left:0;" loading="lazy" decoding="async"/>
  </a>
    </span></p>
<p>I'm grateful to have had the opportunity to attend the first ever Lambda Retreat and hope to carry the functional programming spirit forward. It was super nice meeting all the enthusiastic and kind people at the retreat, and I hope to see everyone again at future events.</p>
<p>Thanks to Anand for organising it and to everyone who attended for making it an enjoyable experience. Thanks also to Madhav and his team at TVC for ensuring our stay was comfortable.</p>
<hr/>
<p>Check out our series on Multicore OCaml, a project I've worked on for the last several years, starting with the <a href="https://tarides.com/blog/2022-12-19-ocaml-5-with-multicore-support-is-here">announcement of the OCaml 5 release</a>. If you'd like to know more about OCaml 5, you can start with <a href="https://youtu.be/6BhmRz7eqiE">KC's keynote address</a> from the ICFP 2022 conference, <a href="https://ocaml.org/docs">OCaml tutorials</a>, and the informative book <a href="https://www.cambridge.org/core/books/real-world-ocaml-functional-programming-for-the-masses/052E4BCCB09D56A0FE875DD81B1ED571"><em>Real World OCaml</em></a>.</p>
<blockquote>
<p><a href="https://tarides.com/company">Contact Tarides</a> to see how OCaml can benefit your business and/or for support while learning OCaml. Follow us on <a href="https://twitter.com/tarides_">Twitter</a> and <a href="https://www.linkedin.com/company/tarides/">LinkedIn</a> to ensure you never miss a post, and join the OCaml discussion on <a href="https://discuss.ocaml.org/">Discuss</a>!</p>
</blockquote>