# Myrrah privacy policy

What Myrrah holds about you, where it is kept, and how to take it back.

> How to read this: the table answers most of it. The sections below say the
> same things with the reasoning attached. Last updated 2026-10-31.

## At a glance

| | |
|---|---|
| Who runs Myrrah | The two people who build it. There is no company behind it yet. |
| What identifies you | An email address, or an Apple or Google sign-in, which nobody else sees |
| What others see | Your first name, your photo if you add one, your score |
| Your location | Asked once, only if you choose, to name your city. Never kept |
| How to get a copy | Profile → Your data → Export my data |
| How to erase it | Profile → Your data → Delete my account |

## A rating is personal data about the person rated

This is the part most products in this shape leave vague, so it is first.

When somebody gives you three stars, that star is **personal data about you**
under both the GDPR and Turkish KVKK — not about the person who gave it. It
describes you, it is attached to your identity, and it affects how others see
you.

Two consequences follow, and the product is built around them:

- **You consented to be rated, as a separate act.** Not buried in a terms
  checkbox. The exact wording you agreed to is recorded against your account
  along with its version, so there is a record of what you were actually told.
- **Ratings about you are yours to export**, even though somebody else wrote
  them.

The person who gave the rating also has an interest in it, as its author. That
is why deleting your account removes the ratings you **gave** as well as the
ones you received.

## What is collected

**An email address.** It is how you sign in: a six digit code is sent to it, or
Apple or Google confirms it for you. It is never shown to another user, never
used as a public identifier, and never appears in a web address. It is held by
the authentication service and is not copied into the part of the database the
app reads from. With Apple you can choose to share a private relay address
instead of your own.

If you sign in with Google, Google also sends your name and a link to your
Google profile picture, and the authentication service keeps what it sends with
your account. With Apple, the first name you give Apple is kept the same way.
Myrrah uses either only to suggest your first name when you set up your
profile; what you type there is what other people see.

If you sign in but never finish setting up your profile, the account and its
address are deleted after 24 hours.

**A first name and, optionally, a photo.** Both are shown to people you meet.
You can add, change or remove the photo in Profile, or skip it entirely.

Your phone's own photo picker hands Myrrah the one photo you choose; the app
never sees the rest of your library. Before that photo leaves your phone it is
made smaller, at most 512 pixels on its longest side, and saved again as a new
file, and everything a phone stores alongside a picture is removed: where it
was taken, when, and on what camera.

The photo is stored in a private bucket. It is not reachable by guessing a URL,
only signed-in users can load it, and only while they can see your profile, so
someone you have blocked, or who has blocked you, cannot. Changing your photo
deletes the old one, and removing it deletes it.

**Your year of birth.** Used once, to check you are 18 or over. The year is
kept; your date of birth is never asked for.

**Your city and country, if you give them.** Used to place you in a
city-level comparison pool and nothing else. They are optional: you are asked
once when you set up your profile, and you can change or remove them at any
time under Profile → Update my city.

You can type your city, or press "Use my location". Only then does Myrrah ask
your phone for its location, and only for an approximate one: on iPhone it asks
for approximate location rather than precise, and on Android it cannot ask for
precise location at all. The maps service built into your phone (Apple's on an
iPhone, and on most Android phones Google's) turns that position into a city
name and a country. You see the result and can correct it before anything is
saved.

Myrrah keeps the city name and the two-letter country code, and nothing else
from this. The position itself is never stored, never sent to Myrrah and never
written to a log. Myrrah does not track where you are, does not ask for your
location in the background, and does not ask again unless you press the button
again.

Nobody else can see your city. No screen shows it to anyone else, and the
database refuses it to every app but yours.

**Ratings, and who you met.** For each encounter: the two people, when it
happened, how it was started, and the star each person gave. There is no
comment field anywhere in Myrrah, by design — a free-text box attached to a
named person is a harassment vector that two people cannot moderate.

**Reports you file.** Including the reason you wrote, which is the only free
text in the product. It goes to the two of us and is never shown to the person
reported.

## What is not collected

No contacts. No address book. No email. No precise location, no background
location, and no record of where you have been. No advertising identifiers. No third-party analytics or tracking SDKs. Myrrah does
not sell data, does not share it with advertisers, and has no advertisers.

Application logs deliberately contain no names, email addresses, photo paths or
coordinates.

## Where it is kept

On Supabase infrastructure in Frankfurt (Postgres, with authentication and file
storage). Access is controlled per row and per column in the database rather
than by the app choosing what to ask for, so a bug in the app cannot hand
somebody another person's data.

### Who else handles it

Two other services take part in signing in, and each receives only what is
listed here.

- **Resend** sends the email with your sign-in code, through Amazon's mail
  service in Ireland. It receives your email address and the code.
- **Cloudflare Turnstile** runs the security check on the sign-in screen, which
  stops scripts from requesting codes in bulk. It sees your phone's network
  address and technical details of the browser view the check runs in. It does
  not receive your email address.

One more takes part only if you press "Use my location":

- **Your phone's maps service** (Apple on an iPhone, and on most Android phones
  Google) receives your approximate position from your phone's operating system
  and returns the name of the place. Myrrah does not send it anything; this
  happens under Apple's or Google's own privacy terms.

And one receives a report when the app crashes or hits an error:

- **Sentry** receives crash and error reports, in its EU data region
  (de.sentry.io, Frankfurt). A report holds the error, where in the code it
  happened, the phone model and system version, the app version, and the
  network calls made just before it, cut down to their shape: the address
  without its search terms, the method and the result code. It is built to
  hold none of your name, email address, photo, city, location, network
  address or anything typed into the app; those are removed on your phone
  before the report is sent. Reports from the iPhone and Android crash
  handlers carry a random identifier for this installation of the app, which
  is not linked to your account and changes if you reinstall. No screenshots,
  no recordings of the screen, no usage tracking.

## Who can see what

| Data | Who sees it |
|---|---|
| Your email address | Nobody but you. Not other users, not us in normal use |
| Your name, photo, score | Signed-in Myrrah users |
| Whether your account is suspended | Signed-in users' apps, which show it only as an absence. Never the reason |
| Your year of birth and your consent record | You, in your export. Not other users |
| Your city and country | You. Not other users, and no screen shows them to anyone else |
| A rating you were given | You, after a short delay, and in your export |
| A rating you gave | You, and the person you gave it to |
| Who you met | You and the person you met |
| A report you filed | The two of us. Never the person reported |

You are never shown a ranked list of people, and no part of Myrrah will tell
you where you sit relative to a specific person. Standing is a band — "top ten
percent" — and that is a deliberate limit on what the product is willing to
compute about anyone.

## Taking a copy

**Profile → Your data → Export my data.**

You get one document containing your profile, your score, every rating you were
given, every rating you gave, every encounter, and the circles you are in. It
arrives through your phone's share sheet, so you choose where it goes.

## Erasing it

**Profile → Your data → Delete my account.**

Without the app, email tarkan.suravwrk@gmail.com from the address you sign in
with and ask for your Myrrah account to be deleted. It is deleted the same way,
and you get a reply once it is gone.

This removes your profile, your photo, your encounters, every rating you were
given, and every rating you gave. Because the ratings you gave are removed, the
people you rated have their scores recalculated without them.

Your photo is deleted first. If that fails, nothing else is deleted either, and
you can try again.

It is immediate and it cannot be undone. There is no grace period and no way to
recover the account afterwards.

Your email address is released at the same time, so it can be used to start a
new account later.

> **Note.** One exception, stated plainly: if you have been suspended and have an open
> appeal, deleting your account ends the appeal, because the record it would
> have been investigated against goes with it.

## Keeping you to one account

An email address, an Apple account or a Google account can hold one Myrrah
account at a time. That is a weaker limit than it sounds: making several email
addresses is easy. What protects a score today is that every rating needs a
handshake in person, and that one person can rate another only once. If a
stronger check is added, this section will say what it collects.

## Children

Myrrah is for people aged 18 and over. The check happens when you set up your
profile, before it exists, and is enforced by the database, not only by the
app. An account that fails it is deleted at once. We do not
knowingly hold data about anyone younger; if you believe we do, contact us and
it will be deleted.

## Changes to this policy

The consent wording has a version recorded against your account. If the wording
changes in a way that changes what you agreed to, the version changes with it
and you will be asked again rather than silently moved onto new terms.

## Contact

By email at tarkan.suravwrk@gmail.com, which is also the address on the store
listing, or through the repository. There is no support desk; there are two
people.
