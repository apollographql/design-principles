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
