---
layout: page
title: Pricing
permalink: /pricing/
description: <b>In Your Face PREMIUM</b> removes all limits and you'll never miss another important meeting again. Plus, you'll be supporting the continued development of the app.
features:
  - text: Full screen event alerts for all your calendar events and Apple Reminders
  - text: Current and upcoming events in the menu
  - text: Join video calls directly from an alert or the menu
  - text: Snooze alerts
  - text: Create reminders in the app
  - text: Preview the upcoming event in the menu bar, with countdown
  - text: Customize alert settings for each event
  - text: Custom snooze durations
  - text: Alert sounds
  - text: Siri Shortcuts and Focus Filters

faq:
  - question: Why subscriptions?
    answer: Continuously improving the app, adding new features or answering support requests takes a lot of time and effort. This is not a hobby project, it is my job. Building and maintaining a sustainable business is only possible with recurring revenue.
  - question: What happens when the free trial ends?
    answer: After you have exhausted the included free alerts of the trial the app will no longer show you any alerts.
  - question: What happens if I cancel the subscription?
    answer: You will still be able to use the app until the end of the subscription term. After that the app will no longer show you any alerts.
  - question: Can I get a refund?
    answer: If you don't like the app or it does not work for you then you can <a href="https://support.apple.com/en-us/HT204084">request a refund from Apple</a>. Developers can not directly issue refunds for app bought in the App Store. In case you bought a lifetime license please contact <a href="mailto:iyf@bluebanana-software.com">iyf@bluebanana-software.com</a>.
  - question: What if I bought the app before the switch to the subscription model?
    answer: Users who bought the app before the switch to the subscription model (August 2022) can make full use of the app without restrictions.
  - question: Do I need a special version for the lifetime license?
    answer: Yes! The lifetime license is only available with the non-App Store version of In Your Face <a href="https://bluebanana-software.com/iyf/InYourFace.zip">(download here)</a>. All different versions of the app have the exact same functionality and will receive all updates at the same time.
  - question: Questions?
    answer: Contact us for any further questions at <a href="#">iyf@bluebanana-software.com</a>.

pricing_table:
  - name: Monthly Subscription
    color: "#eee"
    price: "$&thinsp;1.99"
    term: "per month<sup>1</sup>"
    call_to_action:
      link: https://apps.apple.com/app/in-your-face/id1476964367
      text: Go to App Store
  - name: Yearly Subscription
    color: "#eee"
    highlighted: true
    price: "$&thinsp;19.99"
    term: "per year<sup>1</sup>"
    call_to_action:
      link: https://apps.apple.com/app/in-your-face/id1476964367
      text: Go to App Store
  - name: Lifetime License
    color: "#eee"
    price: "$&thinsp;59.99"
    term: "one-time purchase<sup>2</sup>"
    call_to_action:
      link: ../buy
      text: Buy Now
---

<div class="plans">
	{% for plan in page.pricing_table %}
		<ul class="plan {% if plan.highlighted %}highlighted{%endif %}">
			<li>
				<h3>{{ plan.name }}</h3>
        <h2>{{ plan.price }}</h2>
        <p class="term">{{ plan.term }}</p>
      </li>

			<!-- {% for feature in plan.features %}
				<li {% if feature.highlight %} class="highlighted"{% endif %}>{{ feature.text }}</li>
			{% endfor %} -->

			{% if plan.call_to_action %}
				<li class="pricing-cta">
          <div class="button">
            <a style="background: {{ plan.color }}" href="{{ plan.call_to_action.link }}">{{ plan.call_to_action.text }} &rarr;</a>
          </div>
        </li>
			{% endif %}
		</ul>
	{% endfor %}
</div>

<footnote class="pricing">
  <i><sup>1</sup>Pricing applies to the U.S. App Store. Local pricing may differ.</i>
  <i><sup>2</sup>Pricing applies to the U.S. Local pricing and application of sales taxes may differ.</i>
</footnote>

<div>
{% if page.faq %}
    <h2>Subscriptions FAQ</h2>
    <dl class="faq">
        {% for item in page.faq %}
            <div>
                <dt>{{ item.question }}</dt>
                <dd>{{ item.answer }}</dd>
            </div>
        {% endfor %}
    </dl>
{% endif %}
</div>