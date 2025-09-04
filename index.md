---
title: SD Bullion – FAQ
layout: home
---
<input id="search-input" type="search" placeholder="Search the FAQ (e.g., cancel, wire, tube)" style="width:100%;max-width:700px;padding:10px;margin:16px 0;">
<ul id="results"></ul>

<script src="https://unpkg.com/simple-jekyll-search@latest/dest/simple-jekyll-search.min.js"></script>
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results'),
    json: '{{ site.baseurl }}/search.json',
    // Show a snippet of matching page text:
    searchResultTemplate: '<li><a href="{url}">{title}</a><br><small>{content}</small></li>',
    noResultsText: '<li>No results found.</li>',
    fuzzy: true,
    limit: 10,
    // Trim the content so it’s a short snippet:
    templateMiddleware: function(prop, value, template) {
      if (prop === 'content') {
        return value.length > 180 ? value.substring(0, 180) + '…' : value;
      }
      return value;
    }
  });
</script>

<script>
  const input = document.getElementById('search-input');
  const catList = document.getElementById('category-list'); // add id to your category <ul>
  input.addEventListener('input', () => {
    if (!catList) return;
    catList.style.display = input.value.trim() ? 'none' : '';
  });
</script>



# SD Bullion – Frequently Asked Questions

Browse by category:

- [Payments & Transactions]({{ site.baseurl }}/payments/)
- [Orders & Shipping]({{ site.baseurl }}/orders/)
- [Products & Inventory]({{ site.baseurl }}/products/)
- [Pricing & Deals]({{ site.baseurl }}/pricing/)
- [Accounts & Depository]({{ site.baseurl }}/accounts/)
- [Sweepstakes & Promotions]({{ site.baseurl }}/sweepstakes/)
- [Website & Checkout]({{ site.baseurl }}/website/)
