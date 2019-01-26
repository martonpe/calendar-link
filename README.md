# Calendar Link

[![Greenkeeper badge](https://badges.greenkeeper.io/AnandChowdhary/calendar-link.svg)](https://greenkeeper.io/)
[![Travis](https://img.shields.io/travis/AnandChowdhary/calendar-link.svg)](https://travis-ci.org/AnandChowdhary/calendar-link)
[![Coverage Status](https://coveralls.io/repos/github/AnandChowdhary/calendar-link/badge.svg?branch=master)](https://coveralls.io/github/AnandChowdhary/calendar-link?branch=master)
[![GitHub](https://img.shields.io/github/license/anandchowdhary/calendar-link.svg)](https://github.com/AnandChowdhary/calendar-link/blob/master/LICENSE)
![Vulnerabilities](https://img.shields.io/snyk/vulnerabilities/github/AnandChowdhary/calendar-link.svg)
[![Made in Enschede](https://img.shields.io/badge/made%20in-Enschede-brightgreen.svg)](https://cityofenschede.com/)

JavaScript library to generate an event link for Google Calendar, Yahoo! Calendar, Microsoft Outlook, etc.

[![NPM](https://nodei.co/npm/calendar-link.png)](https://npm.im/calendar-link/)

### Usage

```js
import calendarLink from 'calendar-link'

// Set event as an object
const event = {
  title: 'My birthday party',
  description: 'Be there!',
  starts: '2019-12-29 18:00:00 +0100',
  duration: [3, 'hours']
};

// Then fetch the link
calendarLink.google(event); // https://calendar.google.com/calendar/render...
calendarLink.outook(event); // https://outlook.live.com/owa/...
calendarLink.yahoo(event); // https://calendar.yahoo.com/?v=60&title=...
```

### Options

| Property | Description | Allowed values |
| --- | --- | --- | --- |
| `title` 👍 | Event title | String |
| `start` 👍 | Start time | [JS Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) / [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) / Unix Timestamp |
| `end` 🤙 | End time | [JS Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) / [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) / Unix Timestamp |
| `duration` 🤙 | Event duration | Array with value (Number) and unit (String) |
| `description` 👌 | Information about the event | String |
| `location` 👌 | Event location in words | String |
| `busy` 👌 | Mark on calendar as busy? | Boolean |
| `guests` 🤞 | Emails of other guests | Array of emails (String) |

#### Support key

| Emoji | Meaning |
| --- | --- |
| 👍 | Required |
| 🤙 | Any one is required |
| 👌 | Supported but not required |
| 🤞 | Not all calendars support |

## License

MIT © [Anand Chowdhary](https://anandchowdhary.com/?utm_source=github&utm_medium=calendar-link&utm_campaign=readme)
