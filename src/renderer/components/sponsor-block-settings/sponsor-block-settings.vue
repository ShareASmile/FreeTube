<template>
  <ft-card
    class="relative card"
  >
    <h3
      class="videoTitle"
    >
      {{ $t("Settings.SponsorBlock Settings.SponsorBlock Settings") }}
    </h3>
    <ft-flex-box class="sponsorBlockSettingsFlexBox">
      <ft-toggle-switch
        :label="$t('Settings.SponsorBlock Settings.Enable SponsorBlock')"
        :default-value="useSponsorBlock"
        @change="handleUpdateSponsorBlock"
      />
    </ft-flex-box>
    <ft-flex-box class="sponsorBlockSettingsFlexBox">
      <ft-toggle-switch
        :label="$t('Settings.SponsorBlock Settings.Notify when sponsor segment is skipped')"
        :default-value="sponsorBlockShowSkippedToast"
        @change="handleUpdateSponsorBlockShowSkippedToast"
      />
    </ft-flex-box>
    <ft-flex-box>
      <ft-input
        :placeholder="$t('Settings.SponsorBlock Settings[\'SponsorBlock API Url (Default is https://sponsor.ajay.app)\']')"
        :show-arrow="false"
        :show-label="true"
        :value="sponsorBlockUrl"
        @input="handleUpdateSponsorBlockUrl"
      />
    </ft-flex-box>
  </ft-card>
</template>

<script src="./sponsor-block-settings.js" />
<style scoped src="./sponsor-block-settings.css" />
