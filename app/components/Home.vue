<template>
  <Page>
    <ActionBar>
      <Label text="Home" />
    </ActionBar>

    <GridLayout>
      <Label class="info">
        <Page loaded="pageLoaded">
          <ActionBar title="My App" class="action-bar"></ActionBar>
          <Image
            src="https://user-images.githubusercontent.com/544280/42960643-66d498ac-8b5a-11e8-8946-7224eefea6a5.jpg"
          ></Image>
        </Page>
        <FormattedString>
          <Span class="fas" text.decode="&#xf135; " />
          <Span :text="message" />
        </FormattedString>
      </Label>
    </GridLayout>
  </Page>
</template>

<script>
import "~nativescript-theme-core/css/sky.css";

export default {
  computed: {
    message() {
      return "Hello World!";
    }
  }
};
</script>

<style scoped lang="scss">
@import "~@nativescript/theme/scss/variables/blue";

// Custom styles
.fas {
  @include colorize($color: accent);
}

.info {
  font-size: 20;
  align-items: center;
  vertical-align: center;
}

@keyframes spin {
  from {
    transform: rotate(0);
  }
  to {
    transform: rotate(360);
  }
}
image {
  animation-name: spin;
  animation-duration: 3s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}
</style>
