+++
title = "MS Bookings"
date = "2025-12-09"
description = "An introduction to MS Bookings from our wonderful training team"

[taxonomies]
tags = ["microsoft", "internalTraining"]
+++

Sean showed us [MS Bookings](https://outlook.office.com/bookings/homepage), this is a tool from Microsoft to make it easier to book appointments. Users can set up spans of time and others can create appointments in these windows. While it works with Outlook, it is not part of Outlook so it's a bit less tightly integrated than it could be.

## Making a booking

The main parameters to provide
- Title and Description: so it's clear what these bookings are for
- Category: these are the ones in Outlook, letting you filter you calendar
- Location: this will suggest locations from general map information, it doesn't integrate with the organisations room booking data. It can also accept free text.
- Teams meeting toggle: to add a Teams link to these bookings
- Duration: 15, 30, 45 minutes and 1 hour are suggested by default but a custom value can be given.
- Public/Private: When the booking is Public it will be shown on your personal booking page. Private bookings can only be accessed via a direct link, which allows you to manage access to it.

### Extra settings

#### Schedule
By default Bookings will "Use my regular meeting hours" the information from Outlook Settings (Calendar -> Work hours and location). You can switch this to a customised schedule which lets you specify the hours of the days to offer. These can be limited to a given start and end date.

#### Buffer times

To protect you from back to back meetings, you can add an optional 5min to 3 hours between bookings. This is clear but the "Limit start time to" defaults to 30 minute intervals.


{{ admonition(type="info", title="Todo" text="Experiment with combinations of durations, buffers and start time limits. Concerned that the wrong mix could block out too much time") }}

#### Lead times

This lets you limit how soon or how far away you can book an appointment.

{{ admonition(type="info", title="Todo" text="Check if invalid combinations of buffer windows and schedule start/end times are detected and prevented.") }}

#### Emails

You can create one or more emails with a rich text message before the event as a reminder, you can also send follow ups in the same way. These options go between 15 mins and 2 weeks.


## Limitations

### Bookings doesn't protect its windows

There is no indication if someone tries to book a normal meeting during these times. I checked in both the basic event creation window and the meeting scheduler.

## Questions

- Is the booking fully public or org level?
