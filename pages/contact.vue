<script>
import feather from "feather-icons";
import GoogleMapsDisplay from "@/components/contact/GoogleMapsDisplay";
import ContactDetails from "@/components/contact/ContactDetails";

export default {
  scrollToTop: true,
  components: {
    GoogleMapsDisplay,
    ContactDetails
  },
  data: () => {
    return {
      contacts: [
        {
          id: 1,
          name: "Landsbergerstraße 71, 82205 Gilching",
          icon: "map-pin",
        },
        {
          id: 2,
          name: "fabian[at]web-brandings.de",
          icon: "mail",
        },
        {
          id: 3,
          name: "+49 177 639 7211",
          icon: "phone",
        },
      ],
    };
  },
  mounted() {
    feather.replace();
  },
  updated() {
    feather.replace();
  },
};
</script>

<template>
  <div
    class="
      container
      mx-auto
      flex flex-col-reverse
      md:flex-row md:py-10 md:mt-20
    "
  >
    <!-- Contact form -->
    <!-- TODO: <ContactForm />-->

    <!-- Google Maps -->
    <GoogleMapsDisplay />

    <!-- Contact details -->
    <ContactDetails :contacts="contacts" />
  </div>
</template>
