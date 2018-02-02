<template>
  <div>
    <mage-change></mage-change>
    <center></center>
    <fast></fast>
    <take-ticket></take-ticket>
    <last></last>
  </div>
</template>
<script>
import mageChange from "./title/mageChange";
import center from "./content/center";
import fast from "./fast/fast";
import takeTicket from "./buy/takeTicket";
import last from "./last/last";

export default {
  components: {
    mageChange,
    center,
    fast,
    takeTicket,
    last
  }
}

</script>
