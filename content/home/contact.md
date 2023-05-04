---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: true

# Contact details (edit or remove options as required)
  email: nicholas.owen1 [@] gmail.com
  #phone: 888 888 88 88
  address:
    street: 11-43 Bath St.
    city: London
    region: UK
    postcode: "EC1V 9EL"
    country: United Kingdom
    country_code: UK
  coordinates:
    latitude: "51.527477097727406"
    longitude: "-0.09110300317931835"
  #directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
  #office_hours:
  #  - 'Monday 10:00 to 13:00'
  #  - 'Wednesday 09:00 to 10:00'
  #appointment_url: 'https://calendly.com'
  contact_links:
    - icon: twitter
      icon_pack: fab
      name: DM Me
      link: "https://twitter.com/Dr__NO"
    - icon: video
      icon_pack: fas
      name: Zoom Me
      link: "https://zoom.com"

design:
  columns: "2"
---