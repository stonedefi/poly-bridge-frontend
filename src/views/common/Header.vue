<template>
  <div class="header">
    <CLink class="brand" :to="{ name: 'home' }">
      <img
        class="brand-logo"
        src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAO0AAAA8CAMAAAC98c03AAAANlBMVEVHcEwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAADAR2LVAAAAEXRSTlMAuh3s+V8qBxA73krKm6+HdEtF8j8AAASTSURBVGje7ZrZkuMqDEDDEiPv5v9/9t4stpEiCfAkPSn3qKofOnEMBwltcLn8k5uMMcbpl7C28SHLL2C1cZf+7LBDTKU5NesVsUZnz7xhPYZtT8zaYCOO1xOzhgmzmiPvgKZp7E3gKWH9RpTk101/RdLagN6OH5c+zw1zkx6zdnjDwjSGvG2Y+CK+4dxBZNw+3H9NtpKfk2G72wevUaK5/2bNDmDgh5lkVk827FwQfUPHjvIwES/TDhd9PbZlh8f/QAd+2uTKLr1nWzbryHIHNtlQnRaoMDJs7O4PLPIDgEdwQsikkxVeA0QpI1m9IOs8eciptD5Da5XlcAGvJ7VlU0YbuFXtQNOaKYzTtbodlQdWPKDKrqO9/Qoc51QkWi+mVqLyTIlug49ZW9/n0R3WLe8fBdq2KLfm/N2ia24bYk5k2Vw8ncf1AK2hJpaaaXil1SrAnjpQUZ62NLOL1fMO48XGQp621XXiku1gjbeEdlDj7VJcRHjOATSs0gDDJbQuT3tVrbQh4bVHz/gMxlScWMd30KIH62lnoO41ofVxySVS5bRv0S2y5VraNMKuZVAyb5vuxp416R+ndUdob/u2S6y0cbr/va1F8w20yaNVuk0mCEYPRo+Mu/8K2t2Wy2kviQ2HRQ+96/ft36XtaI5RQZsYtdcbUtv3HNH8cxHoOhN9HKElmepMbWBSM6q+uEf5x7TzloaCRruUN9+6IOhOItqqyqF7iJl7Gz5CO26fGzVzXGfykIYpYAV7bLOtuaAlye+mJV6iKE92uNOxC00l6PdwUTYuHQQ+QXtBXxTRer6WNySxt5laX1Xu/6PAJ2ibtFAp1y2QRqMjRgyksTZAbc03fIIWxYBy3XqdddbXAuM6va30Vtpt4lW6VWt50ojMpg6W7TouH6G1u18uou0J7cKmifL3QusRbHMX2/J9lTfRbhU1kA5rq8TJfXsFPQIP9ecGke2Ivot2b2xMxbnUuoet7mN9uBym9Z+h3bDGsZL2GvRmOOqmj/AdtNtBs6uiNVZv/U+ADbz9EloS4otohagCbNTpK24nfJyWuN8CWoM+tMYEPBLKdJ8R5lt0+zj0q6F9ySUsGmnhar6v0S12LnW0LWp/A6lxk8bG9+gW5T81tGtxsHmsOW26olPR5nto0wtAFbRz1I428HFlZQQqyS74kxFgT0ZGIXQU07bMSbjYxBlyr1CuAORooxl2mVyeNrHl3ERa5uzeii2ndT58WjWItE0BLQqdXigaWdp94BztxLQdrN6JFA/nO5G2pL6VWh/cafV40cxdpn2OaAfx7J3WrKO4GbrclRn11Eu8tZEWUTztZnuFut0LU6I52tgwSm0g0S5CHTJkamn5lsl48JaJIU4GzyyQms/bkkO+mDvsd8Kc+2xjC4T1g7IbRGjEnhRC5Mpj7gDXdi/OxZueMYa28865zjIHL0yrZ0itbbz9kumM3V+5LcLsOPGDoixwBRcyXuar3bUregFYJHDgHQdk0jvMn5SQ/P2IXHM3qE4kpDHsz33Z3v6aO8oPH+4KjgZOJK10ZHVSWU6/YV8jwbnkP2ZuLJKrZhRxAAAAAElFTkSuQmCC"
      />
    </CLink>
    <a href="https://www.stonedefi.io/" class="brand-name">{{ $t('common.header.brandName') }}</a>
    <CFlexSpan />
    <Menu />
    <Wallets />
    <Networks />
  </div>
</template>

<script>
import Wallets from './Wallets';
import Networks from './Networks';
import Menu from './Menu';

export default {
  name: 'Header',
  components: {
    Wallets,
    Networks,
    Menu,
  },
};
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  align-items: center;
  height: 80px;
  padding: 0 50px;
  @include child-margin-h(20px);
}
.brand-logo {
  width: 120px;
}
.brand {
  display: flex;
  align-items: center;
  @include child-margin-h(30px);
}

.brand-name {
  padding-left: 16px;
  color: unset;
  text-decoration: none;
  font-size: 20px;
}
</style>
