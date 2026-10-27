# Subscription page brand icons

This overlay customizes only the favicon tags in the index template from
`remnawave/subscription-page:8.0.0`. The application and its upstream assets are
unchanged. Upstream source and license: https://github.com/remnawave/subscription-page.

The selected subscription page's existing `metaTitle` chooses the icons:
`Indy+` uses the approved Indy logo from `IndyPlusService/wiki`, and
`Canvas Proxy` uses the existing Canvas logo. Other titles retain upstream icons.

Deployment: save the published `index-8.0.0.html` as `overrides/index.html` next
to the original Compose file and install the published
`docker-compose.override.yml`. Verify the generated Compose configuration before
recreating only `remnawave-subscription-page`, without pulling an image.
Keep the original configuration and permissions for rollback.

When upgrading the upstream image, regenerate this template from that image's
index file so its frontend asset names remain correct. If subscription meta
titles change, update the corresponding icon selectors.
