<template lang="pug">
v-app
  v-toolbar
    v-toolbar-title {{ $static.metaData.siteName }}
    v-spacer
    v-toolbar-items
      v-btn(flat exact :to="{ name: 'home' }") Home
      v-btn(flat :to="{ name: 'about' }") About

  v-container
    slot
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>
