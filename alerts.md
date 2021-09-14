# Alerts design principles

An alert is a type of notice that displays a short, important message in a way that attracts the user's attention without interrupting the user's task. 

It should be used specifically when the information or actions it contains is relevant to the users immediate actions or workflow (as opposed to notifications, audit logs, or other more persistent information).

Alert types and their usage:

## :information_source: Informational

Informational alerts present general info about something you are doing or working with. It is neutral and conveys no implications of success or failure.

**When to use:** Use when further information is available about the users action or workflow that is relevant to what they are doing and not otherwise obvious in the UI.

**Style:**
- color association: blue
- icon: [IconInfoSolid](https://space-kit.netlify.app/?path=/story/components-icons--icon-info-solid)

## :warning: Warning

Warning alerts present information about the action that is about to be taken that alerts the user to consequences of the action and asks for confirmation that the action still be taken in light of the consequences.

**When to use:** Use in any instance where it would be best to ensure the user is fully informed of the implications of the action, especially if the action may be destructive or irreversible.

**Style:**
- color association: orange
- icon: [IconWarningSolid](https://space-kit.netlify.app/?path=/story/components-icons--icon-warning-solid)

## :x: Error

Error alerts let the user know that something has gone wrong or is blocked in the given workflow they are trying to complete. When possible, error alerts should contain helpful information about what has happened to help unblock the user (such as steps to resolve or a link to a docs article).

**When to use:** Use when it is not clear from any other available and obvious component in the UI that an action has failed.

**Style:**
- color association: red
- icon: [IconErrorSolid](https://space-kit.netlify.app/?path=/story/components-icons--icon-error-solid)

## :white_check_mark: Success

Success alerts are confirmation that the action the user was trying to take has succeeded.

**When to use:** Use when it is not obvious from any other part of the UI that success has occurred (e.g. in Studio, successfully running an operation results in a visible Response, so a success alert is not necessary).

**Style:**
- color association: green
- icon: [IconSuccessSolid](https://space-kit.netlify.app/?path=/story/components-icons--icon-success-solid)

## :clock3: Neutral

Neutral alerts are intended to provide a passive notification to the user, most often as it relates to the freshness of data, but can be expanded to include additional scenarios.

**When to use:** Use when it is helpful to inform users that settings and/or configurations have changed since the generation of a given artifact.

**Style:**
- color association: gray
- icon: [IconTimeSolid](https://space-kit.netlify.app/?path=/story/components-icons--icon-time-solid)

---

Worthwhile reading for reference:
- [Material UI approach to Alerts](https://material-ui.com/components/alert/)
- [Primer Design System: Messaging](https://primer.style/design/ui-patterns/messaging)
- [Bootstrap Toasts](https://getbootstrap.com/docs/4.2/components/toasts/)
- [Primer Toasts](https://primer.style/css/components/toasts)

---

# Design implementation

Here are some examples for how Alerts can be implemented, starting with the two main use cases:

## Alert banners

Alert banners are primarily for situations where there is nothing you can do in the UI to immediately fix or change the state (e.g. deprecation warnings, account status alerts, etc).

![alert-banners-image-light-and-dark](https://user-images.githubusercontent.com/1319791/133327896-f0346b15-4847-432a-b6f7-aa0916f0ed98.png)


- [see AlertBanner](https://space-kit.netlify.app/?path=/docs/components-alertbanner--info-light) in SpaceKit Storybook.
- see in [Sketch Cloud](https://www.sketch.com/s/aa84f7e1-c1aa-4f8c-a252-b62955de353a/a/ew5w0x), and see also [version with CTA button](https://www.sketch.com/s/aa84f7e1-c1aa-4f8c-a252-b62955de353a/a/l3RVwe)

## Full-page banners

Full-page banners are a form of alert banner reserved for situations where the message pertains to app-level or page-level situations. These banners display a persistent message that cannot be manually dismissed by the user. These banners inherit the same type themes and iconography as standard alert banners, with the addition of a neutral type (gray), used for displaying information about the freshness of page content.

Full-page banners are appended to the base of the page header, and like the page header, should stay fixed in view even if the contents of the page scroll.

|||
|---|---|
|![full-page-alerts-light](https://user-images.githubusercontent.com/1319791/133329067-24c475ce-9dca-4c1f-8e33-5ce5a9b81d8f.png)|![full-page-alerts-dark](https://user-images.githubusercontent.com/1319791/133329098-e8eb6f2b-de05-472c-a56b-0d279482a420.png)|

## Alert toast cards

Toast cards appear in the middle of your workflow when an action you’ve taken prompts a message, or when a state that your account, graph, or data is in prompts a message.

Toast cards can have several variations:
- just a message that can be dismissed
- a message with a primary (and optionally a secondary) call to action button
- or an expanded content variant that allows for longer form instructions or messaging (used when the content requires more than a single paragraph)

|||
|---|---|
|![alert-toast-card-examples-light](https://user-images.githubusercontent.com/1319791/133328528-0ea33b49-334b-4146-b15a-a837138415b1.png)|![alert-toast-card-examples-dark](https://user-images.githubusercontent.com/1319791/133328572-4829de4c-7f6b-4eba-945e-ac5cca8e2c5a.png)|

- [see in AlertCard](https://space-kit.netlify.app/?path=/docs/components-alertcard--info-light) in SpaceKit Storybook.