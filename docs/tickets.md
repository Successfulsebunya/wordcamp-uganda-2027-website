# Tickets

Tickets are sold with **CampTix**, the WordCamp ticketing plugin. Payments go to WordCamp Central, not to the local team.

## Tickets on sale

| Ticket | Price | Shown in UGX | Notes |
| --- | --- | --- | --- |
| Early Bird | USD 15 | UGX 50,000 | Sales end at the end of December 2026 |
| Regular | USD 20 | UGX 70,000 | |

- Prices are charged in **USD**, because PayPal and card payments (Stripe) are processed by WordCamp Central.
- The UGX amount is written in each ticket's description (CampTix only supports one currency), so local buyers know what they're paying.
- Every ticket includes coffee, lunch and swag.
- Tickets can be transferred to someone else.
- Early Bird is listed above Regular.

## How CampTix is set up

| What | Where |
| --- | --- |
| Tickets | Tickets → Tickets (`tix_ticket` post type) |
| Ticket description | The ticket's **excerpt** field |
| Sale end date | Ticket's end date (`tix_end`) |
| Order in the table | Publish date, newest first. To move a ticket up, give it a later publish date |
| Currency | Tickets → Setup → Payment |
| Attendee list | `[camptix_attendees]` on the Attendees page |

A link can open the form with a ticket already chosen:

```
/2027/tickets/?tix_action=attendee_info&tix_tickets_selected%5B<TICKET_ID>%5D=1
```

## Tickets page

The page is kept short: what you get, two tickets, a short FAQ and nothing else.

1. **Intro:** what's included, in two columns
2. **Ticket card:** the `[camptix]` shortcode
3. **Good to know:** three FAQ items in the same Details style as the FAQ page
4. **Notes**

## Form styling

CampTix outputs its own markup, so this is the one place the site needs real CSS (section "CampTix: tickets" in `custom.css`):

- Ticket rows use ink, not yellow, for the side bar and info text, for contrast.
- Quantity select has a custom chevron and a 48px touch target.
- Coupon field and button sit on one line, and stack on small screens. CampTix's script forces the coupon container to `display:block`, so the layout uses inline-block instead of flex.
- Space between the table header and the first ticket.
- Under 768px the table becomes a single column so nothing is cut off. Under 360px the quantity stacks under the price.
- Visible focus outlines on every control.
