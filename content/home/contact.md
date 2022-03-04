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
            captcha: false
    # Contact details (edit or remove options as required)
    #   email: test@example.org
    #   phone: 888 888 88 88
    address:
        street: 828 Boulevard des Maréchaux
        city: Palaiseau
        region: Ile de France
        postcode: "91120"
        country: France
        country_code: FR
    # Geographic coordinates
    # To get your coordinates, right-click on Google Maps and choose "What's here?". The coords will show up at the bottom.
    coordinates:
        latitude: "48.71054981091499"
        longitude: "2.218886947100561"
        
#   directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
#   office_hours:
#     - 'Monday 10:00 to 13:00'
#     - 'Wednesday 09:00 to 10:00'
#   appointment_url: 'https://calendly.com'
#   contact_links:
#     - icon: twitter
#       icon_pack: fab
#       name: DM Me
#       link: 'https://twitter.com/Twitter'
#     - icon: video
#       icon_pack: fas
#       name: Zoom Me
#       link: 'https://zoom.com'

design:
  columns: '2'
---
