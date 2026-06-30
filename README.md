repo:
  name: sunshynelabs.github.io
  owner: sunshynelabs
  branch: main
  deploy_root: /

site:
  type: static
  generator: none
  custom_domain: sunshynelabs.com
  https: enforced

deployment:
  source: main
  root: /
  framework: github-pages

dns:
  domain: sunshynelabs.com
  records:
    - type: A
      values:
        - 185.199.108.153
        - 185.199.109.153
        - 185.199.110.153
        - 185.199.111.153

pages:
  - path: /
    title: Home
    description: Landing page
  - path: /research/
    title: Research
    description: Research overview and product index
  - path: /angel/
    title: ANGEL
    description: Trench-grade automation system
  - path: /sandra/
    title: SANDRA
    description: Deterministic extraction pipeline
  - path: /mary/
    title: MARY
    description: Contact center retention system
  - path: /gabriel/
    title: GABRIEL
    description: Knowledge base training method
  - path: /jack/
    title: JACK
    description: Governed LLM workflow framework
  - path: /ec/
    title: ExCorText UPI v3.7
    description: Repair ticket simulator (demo)
  - path: /404.html
    title: 404
    description: Custom not-found page

build:
  jekyll:
    config: _config.yml
    data: _data/navigation.yml
    required_for_render: false

contact:
  canonical: info@sunshynelabs.com

maintenance:
  warnings:
    - Keep canonical tags and sitemap URLs consistent with sunshynelabs.com
    - JSON-LD structured data is duplicated across product pages
    - ec/ is a contained simulator demo
  actions:
    - Sync JSON-LD when updating product metadata
    - Remove or relocate ec/ to reduce public surface
