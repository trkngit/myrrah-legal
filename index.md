# Myrrah privacy policy

What Myrrah holds about you, where it is kept, and how to take it back.

> How to read this: the table answers most of it. The sections below say the
> same things with the reasoning attached. Last updated 2026-10-30.

## At a glance

| | |
|---|---|
| Who runs Myrrah | The two people who build it. There is no company behind it yet. |
| What identifies you | An email address, or an Apple or Google sign-in, which nobody else sees |
| What others see | Your first name, your photo, your score |
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
The photo is stored in a private bucket: it is not reachable by guessing a URL,
and only signed-in users can load one.

**Your year of birth.** Used once, to check you are 18 or over. The year is
kept; your date of birth is never asked for.

**Your city, if you give one.** Used to place you in a city-level comparison
pool and nothing else. Myrrah does not collect your location, does not use GPS,
and does not know where you are.

**Ratings, and who you met.** For each encounter: the two people, when it
happened, how it was started, and the star each person gave. There is no
comment field anywhere in Myrrah, by design — a free-text box attached to a
named person is a harassment vector that two people cannot moderate.

**Reports you file.** Including the reason you wrote, which is the only free
text in the product. It goes to the two of us and is never shown to the person
reported.

## What is not collected

No contacts. No address book. No email. No GPS or background location. No
advertising identifiers. No third-party analytics or tracking SDKs. Myrrah does
not sell data, does not share it with advertisers, and has no advertisers.

Application logs deliberately contain no names, email addresses, photo paths or
coordinates.

## Where it is kept

On Supabase infrastructure in Frankfurt (Postgres, with authentication and file
storage). Access is controlled per row in the database rather than by the app
choosing what to ask for, so a bug in the app cannot hand somebody another
person's data.

### Who else handles it

Two other services take part in signing in, and each receives only what is
listed here.

- **Resend** sends the email with your sign-in code, through Amazon's mail
  service in Ireland. It receives your email address and the code.
- **Cloudflare Turnstile** runs the security check on the sign-in screen, which
  stops scripts from requesting codes in bulk. It sees your phone's network
  address and technical details of the browser view the check runs in. It does
  not receive your email address.

## Who can see what

| Data | Who sees it |
|---|---|
| Your email address | Nobody but you. Not other users, not us in normal use |
| Your name, photo, score | Signed-in Myrrah users |
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

This removes your profile, your photo, your encounters, every rating you were
given, and every rating you gave. Because the ratings you gave are removed, the
people you rated have their scores recalculated without them.

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

Through the repository or the address on the store listing. There is no support
desk; there are two people.
