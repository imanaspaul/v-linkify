<template>
  <div>
    <div v-html="foramttedText"></div>
  </div>
</template>

<script>
import linkifyHtml from 'linkifyjs/html'

export default /*#__PURE__*/{
  name: 'VLinkify', // vue component name
  props: {
    html: {
      type: String,
      required: true,
      default: `Your text will goes here..`
    },
    classname: {
      type: String,
      required: false,
    }
  },
  computed: {
    foramttedText() {
      return this.convertToLink(this.html)
    }
  },
  methods: {
    // convert to linkify
    convertToLink(data) {
      const markup = data
        .replace(/</g, '&lt;')
        .replace(/((?:href|src)=['"])(.*?)(['"])/g, (matched, prefix, href, suffix) => {
          return `${prefix}<a href="${href}" class=linkifyLink" target="_blank">${href}</a>${suffix}`
        })

      return linkifyHtml(markup, { target: { url: "_blank" } })
    }
  }
};
</script>