--- 
title: Buying ponies from a Drupal App Store
created: 1296245397
categories: 
- Drupal
tags:
- app stores
- Drupal App Store
- drupalappstore
- GPL
- open source
- community ROI
---
<p style="text-align: center; "><img alt="" class="imagecache-fullpost lightbox" src="/sites/bmannconsulting.com/files/imagecache/fullpost/postimages/800px-Great_Wave_off_Kanagawa2.jpg" title=""></p>
<p style="text-align: center; "><span style="font-size:10px;"><em>Is the Drupal App Store idea a great wave that will lift the Drupal community to new heights, or will it crush the community of code collaborators?</em></span></p>
<p>I'm glad we've gone beyond talking about whether <a href="http://www.bmannconsulting.com/archive/themes-and-modules-are-derivatives-and-should-be-licensed-under-the-gpl/">themes and modules should be GPL or not</a>. I think the <a href="http://search.twitter.com/search?q=&amp;tag=drupalappstore&amp;lang=all">drupalappstore</a> discussion is about being able to "fund developers" in a way that goes beyond their hours.</p>
<p>I encourage virtually every business I talk to – whether Drupal focused or not – to figure out a way to make revenue that goes beyond billing for hours. It's the only way to truly scale a business without the boom-and-bust cycles of consulting work.</p>
<p>The main thing that has people scared about the concept of a Drupal App Store (in its theoretical sense) is the fear that Drupal's open, collaborative nature will somehow go away. Counter examples like the Joomla community are held up as the way things will end up if we open this Pandora's Box of commercial tyranny.</p>
<p>In my never ending quest to see Drupal move in a more product-like direction, I think a Drupal App Store would be great for developers and great for end users. But let's define what we mean (or at least, what *I* mean), when I say Drupal App Store.</p>
<p><!--break--></p>
<h2>Funding new modules</h2>
<p>I don't want to talk about funding the creation of new modules. This is a solved problem.</p>
<p>I did the <a href="http://drupal.org/node/20301">first reverse bounty way back in 2005</a>, and there is a <a href="http://drupal.org/node/110998">raising money / reverse bounty page on Drupal.org</a> with links to various platforms that can help you do this. If you want to write a new module and need to get funded to buy yourself the time, then go this route.</p>
<p>For developers who aren't good at marketing, I recommend you build a team that can help you with that side of things. These days, there are larger companies that would be willing to fund the creation of modules "done right" so I don't see an issue raising (literally) tens of thousands of dollars this way.</p>
<p>With that out of the way, let's get to a few other points.</p>
<h2>You can sell GPL code</h2>
<p>See Drupal theme stores as one example. You use a combination of copyrighted material (graphics, CSS, etc.) along with GPL PHP code and you can set whatever terms you like around the copyrighted material. Read the <a href="http://fusiondrupalthemes.com/license">Fusion Drupal Themes license</a> for an example of how to do this.</p>
<p>The other great example that I point to over and over again is <a href="https://www.bravenewcode.com/store/plugins/wptouch-pro/">BraveNewCode's WPtouch Pro™</a>. Once you've read about their product (or "app", if you will), read their <a href="http://www.bravenewcode.com/general/terms/">terms and conditions</a>. In essence, they are using the trademarked name of their WordPress plugin to protect their brand and reputation (which is ultimately what they are selling).</p>
<p>Conveniently, they are even using Drupal as an example – someone could take their code, adapt it to work with Drupal, change all the references to WPTouch Pro™, and so on.</p>
<p>I think this model would work for Drupal with virtually no changes, in terms of the legal pieces of "selling code". What customers are buying is some set of upgrade and support. The customer does this because they value the stability, function, features and so on of this piece of code, and want to support it.</p>
<h2>You need to be selling a complete piece of functionality (a pony)</h2>
<p>I think of the issues that people run into when thinking about what would be *in* a Drupal App Store, is they immediately think about Views or something similar. Some foundational piece of tech that they use all the time to build sites with.</p>
<p>I agree that this piecemeal approach to having to buy foundational elements to get the functionality that you need is not the right type of thing that would be easy to sell in an app store.</p>
<p>(on the other hand, I think someone could set up a Views support or site building support private forum and charge good money for it – this isn't that different from some of the paid training or video tutorial elements that are available today)</p>
<p>But I digress. What someone sells in a Drupal App Store needs to be a complete piece of functionality.</p>
<p>Eric Gundersen of Development Seed <a href="http://twitter.com/ericg/status/30613434223558656">mentioned</a> "I'd buy a map feature for my news site or photo gallery feature for wedding site". This is exactly the sort of drop in functionality that has high value for end users and can be relatively self contained.</p>
<p>And I use the term "end users" here rather loosely. The clients for a Drupal App Store will range from self-hosting enthusiasts who just want to complete their wedding site to design agencies that have limited in-house development resources and want to pay to have a supported solution for a client.</p>
<p>Everyone wants to be able to buy a pony. A set of functionality bundled up with a neat little bow in exactly the color you want is exactly what end users like.</p>
<p>How you bundle / deliver / update / ship this complete piece of functionality is up for discussion. It is a thorny technical issue that is … totally solvable. I happen to think that something like <a href="http://drupal.org/project/features">Features</a> actually *is* a much better fit for an "app" than selling a module.</p>
<h2>What about selling distributions and install profiles?</h2>
<p>I can't even tell you how overjoyed I am that <a href="http://angrylittletree.com/11/01/drupal-8-road-ahead">Eaton is proposing a push towards building a Drupal product codenamed 'Tsunami' for Drupal 8</a>. For one, I'm envisioning the Great Wave image above, only with unicorns instead of horses…</p>
<p>(again with the tangent)</p>
<p>To maintain and update great distributions over time, non-hourly client revenue needs to start coming from distributions.</p>
<p>Distributions are definitely NOT apps. They are both easier and harder. They are a single product that doesn't have to rely on a "host" Drupal site. On the harder side, the distribution developers need to track, test, and continually integrate a host of shifting module dependencies, make sure they're picking the "right" modules, and keep custom themes and functions up to date.</p>
<p>I would like to see the developers of distributions charge for something. Maybe it's a bundle of the distribution and some third party, proprietary web services bundled together. Maybe it's a private support forum. You're not really "selling" the distribution, but it mimics the traditional software model, so a lot of traditional organizations could actually pay for it (when they can't, for example, pay a donation).</p>
<h2>How do we "pay for the plumbing"?</h2>
<p>I swear I've also talked about this a million times. It probably needs a microsite, a manifesto to sign up for, and its own Twitter hashtag to really drive the point home.</p>
<p>Do you get paid to develop Drupal-powered websites for clients? Do you use contributed modules to build those sites?</p>
<p>I don't care if you are building a <a href="http://davehall.com.au/tags/100-drupal-site">$100 site</a> or a $100,000 site. If you are using contributed modules, set aside time or money to give back to the maintainers of those contributed modules.</p>
<p>It will save you money in the long run by investing in the modules that you've built code and themes around. Yes, if you fix a bug / submit a patch, that's paying as well, but it would be great to see actual dollars flowing into the contrib ecosystem.</p>
<p><strong>Everyone that uses Drupal to do paid work should have a costing model and internal policy that includes donating to the maintainers of every contributed module that they use on every site.</strong></p>
<p>What's a good formula to use for this? A percentage might be the most logical. 10% for Drupal contrib has a nice ring to it…</p>
<h2>Is a Drupal App Store a good idea?</h2>
<p>For me, the answer is actually…"no".</p>
<p>That is, I can tell you categorically that I *definitely* don't think it is a good idea to get the Drupal Association enmeshed in some sort of commercial venture to run such a store on drupal.org community infrastructure. We don't want to mix in commercial concerns directly in our community home.</p>
<p>But…</p>
<p>I think the concept of individual developers selling "apps" is a great idea. This may end up with someone deciding there is enough volume / value to set up some centralized store infrastructure, but that's kind of beside the point.</p>
<p>I think there are Drupal businesses out there, whether they are one person developers or full shops, who could make money selling Drupal apps in a model similar (if not identical) to how BraveNewCode sells WPtouch Pro™.</p>
<p>It still involves investment. It means doing marketing. It means creating and maintaining a great product (that basically comes first). But it also holds out the promise of value that end users are willing to pay for, and for a stream of revenue that is not directly tied to hours.</p>
<h2>Didn't you skip the whole discussion about how the Drupal community will collapse when money enters the picture?</h2>
<p>I think the centralized nature of modules and code collaboration on drupal.org is a very good thing. I don't think paid modules have a place there, and that is up to each vendor of apps to build their own reputation and show value for what they are selling on sites of their own.</p>
<p>I think a lot of the support load will actually go down.</p>
<p>Are you an end user having trouble with patches, development releases, etc.? Go grab the pro version that is fully supported.</p>
<p>Instead, issue queues can be filled with people doing what they always do: developers scratching itches together and evolving the code.</p>
<p>Remember: our underlying approach to this CMS that we've been building for over 10 years together has always been "let's build something that sucks less".</p>
<p>Even with apps for sale, this doesn't change. The developers of those apps will still get a better <a href="http://www.bmannconsulting.com/tags/#community ROI">community ROI</a> by investing in the framework layers that everyone can benefit from, and that end users don't care about anyway.</p>
<p>And like a Great Wave, that community investment will continue to raise us to new heights.</p>
