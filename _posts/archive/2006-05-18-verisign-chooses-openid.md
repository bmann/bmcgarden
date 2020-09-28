--- 
layout: post
title: Verisign chooses OpenID
created: 1147939270
categories: 
- identity
- verisign
- SAML
- OpenID
- mesh06
- Canter's Law
- Personal Identity Provider
- InfoCard
- Web 2.0
---
<p><a href="http://blogs.verisign.com/infrablog/2006/05/introducing_the_verisign_perso_1.php">VeriSign chose OpenID</a> for their new &quot;Personal Identity Provider&quot;, aka pip: <a href="http://pip.verisignlabs.com/">http://pip.verisignlabs.com/</a>.</p>  <p>I&#39;m a bit confused. OpenID handily does single sign on. But that&#39;s it. I can understand not deploying a huge SAML stack -- all of those blogs and web apps that they talk about it in the announcement post have no way of easily interoperating with SAML today, aka lack of scripty language support -- but OpenID is fairly limited today. Be interesting to see if VeriSign will push Simple Registration Protocol and/or extend the OpenID &quot;spec&quot; and/or standardize it in some way as DIX is doing (or merge/interoperate/implement DIX?).  </p><p>If I were VeriSign, I would follow this up with support for multiple identity protocols -- that is, after all, <a href="http://blog.broadbandmechanics.com/2005/09/canters_law_1">Canter&#39;s Law</a>: work with everything. You could have a single identity hosted by VeriSign and accessible via a variety of protocols, from OpenID to DIX to SAML to InfoCard.</p>  <p>It certainly is great to see experimentation actually starting to happen in this space. At the <a href="http://www.meshconference.com">Mesh conference</a>, which I&#39;ve just come back from, I heard some rumours about a potential 10M profile installation of DIX. Exciting times...</p>
