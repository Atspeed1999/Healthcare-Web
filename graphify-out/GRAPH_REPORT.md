# Graph Report - .  (2026-07-12)

## Corpus Check
- Large corpus: 206 files · ~1,079,034 words. Semantic extraction will be expensive (many Claude tokens). Consider running on a subfolder.

## Summary
- 46 nodes · 66 edges · 6 communities
- Extraction: 79% EXTRACTED · 21% INFERRED · 0% AMBIGUOUS · INFERRED: 14 edges (avg confidence: 0.9)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Homepage & Content Engine|Homepage & Content Engine]]
- [[_COMMUNITY_About & Founders|About & Founders]]
- [[_COMMUNITY_Contact & Site Shell|Contact & Site Shell]]
- [[_COMMUNITY_Service Offerings|Service Offerings]]
- [[_COMMUNITY_Why We're Different|Why We're Different]]
- [[_COMMUNITY_Client Testimonials|Client Testimonials]]

## God Nodes (most connected - your core abstractions)
1. `Homepage` - 10 edges
2. `services[] data (6/8)` - 10 edges
3. `setupDigitalHealthSections() binder` - 6 edges
4. `values[] data (5 differentiators)` - 6 edges
5. `About page` - 5 edges
6. `Contact page` - 5 edges
7. `Navbar (Home/About/Services/Contact)` - 5 edges
8. `Footer (nav + email + LinkedIn)` - 5 edges
9. `DHA healthcare photography (hero/story/service/team-bg)` - 5 edges
10. `Dr Lucy Buckley (Founder)` - 4 edges

## Surprising Connections (you probably didn't know these)
- `Hero contact form (quick enquiry)` --semantically_similar_to--> `Contact page`  [INFERRED] [semantically similar]
  index.html → contact.html
- `Your critical friend` --semantically_similar_to--> `Your critical friend`  [INFERRED] [semantically similar]
  service.html → index.html
- `About team header + Lucy bio` --references--> `DHA healthcare photography (hero/story/service/team-bg)`  [INFERRED]
  about.html → index.html
- `Services collection (8, auto-cloned)` --shares_data_with--> `services[] data (6/8)`  [EXTRACTED]
  service.html → index.html
- `services[] data (6/8)` --references--> `Your critical friend`  [EXTRACTED]
  index.html → service.html

## Import Cycles
- None detected.

## Hyperedges (group relationships)
- **Eight DHA advisory services** — svc_strategy, svc_investors, svc_ma, svc_critical, svc_servicedev, svc_regulatory, svc_marketing, svc_cso [EXTRACTED 0.90]
- **Five differentiators (Why We're Different)** — val_leaders, val_donedit, val_collective, val_fast, val_friend [EXTRACTED 0.90]
- **Inline JS content/data layer** — setup_fn, services_data, team_data, values_data, testimonials_data, faqs_data [EXTRACTED 0.90]
- **Universal nav/footer shell** — navbar, footer, index_home, about_page, service_page, contact_page [EXTRACTED 0.85]

## Communities (6 total, 0 thin omitted)

### Community 0 - "Homepage & Content Engine"
Cohesion: 0.33
Nodes (11): Get in Touch CTA, DHA healthcare photography (hero/story/service/team-bg), FAQ section, faqs[] data, Homepage, Homepage services showcase (6 cards), setupDigitalHealthSections() binder, Story stat slider (infinite loop) (+3 more)

### Community 1 - "About & Founders"
Cohesion: 0.32
Nodes (8): About page, About story + success stats, About team header + Lucy bio, Credentials (CQC / NHS CSO / MRPharmS / PhD), The Digital Health Assurance Company, Dr Lucy Buckley (Founder), Nitin Makadia (Director), team[] data

### Community 2 - "Contact & Site Shell"
Cohesion: 0.32
Nodes (8): Contact form (mailto submit), Contact page, Footer (nav + email + LinkedIn), Hero contact form (quick enquiry), Legal pages (privacy/terms/cookies/licenses/404), Navbar (Home/About/Services/Contact), Services page, Services collection (8, auto-cloned)

### Community 3 - "Service Offerings"
Cohesion: 0.29
Nodes (8): services[] data (6/8), Clinical Safety Officer, Investors, Mergers & acquisitions, Marketing, Regulatory, Service development, Strategy & growth

### Community 4 - "Why We're Different"
Cohesion: 0.29
Nodes (7): Your critical friend, Our collective experiences, We've been there and done it, Fast responses, Your critical friend, Access to industry leaders, values[] data (5 differentiators)

### Community 5 - "Client Testimonials"
Cohesion: 0.50
Nodes (4): Dr Alex Barber, The GP Service, James Chapman, CEO decently, Avihu Tamir, CEO Kanabo, testimonials[] data (real quotes)

## Knowledge Gaps
- **15 isolated node(s):** `About story + success stats`, `Contact form (mailto submit)`, `faqs[] data`, `Strategy & growth`, `Investors` (+10 more)
  These have ≤1 connection - possible missing edges or undocumented components.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Homepage` connect `Homepage & Content Engine` to `Contact & Site Shell`?**
  _High betweenness centrality (0.388) - this node is a cross-community bridge._
- **Why does `services[] data (6/8)` connect `Service Offerings` to `Homepage & Content Engine`, `Contact & Site Shell`, `Why We're Different`?**
  _High betweenness centrality (0.339) - this node is a cross-community bridge._
- **Why does `Homepage services showcase (6 cards)` connect `Homepage & Content Engine` to `Service Offerings`?**
  _High betweenness centrality (0.243) - this node is a cross-community bridge._
- **Are the 6 inferred relationships involving `setupDigitalHealthSections() binder` (e.g. with `Get in Touch CTA` and `FAQ section`) actually correct?**
  _`setupDigitalHealthSections() binder` has 6 INFERRED edges - model-reasoned connections that need verification._
- **What connects `About story + success stats`, `Contact form (mailto submit)`, `faqs[] data` to the rest of the system?**
  _15 weakly-connected nodes found - possible documentation gaps or missing edges._