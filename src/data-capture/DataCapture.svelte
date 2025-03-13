<script lang="ts">
  import { sdkManager } from "@/sdkManager/sdkManager";
  import { onMount } from "svelte";

  onMount(async () => {
    await sdkManager.configure(
      import.meta.env.SCANDIT_LICENSE_KEY ?? "ArwVYhAHNo8xLhGzE9PgNC4x3h3gN0BBNAg07OsRKxrYIxJ2fFZdaQZFAVB+MOWG6nXuc2xcEWjCP2zzdGqIQUpTsELSWeDkWlQr0zgHGh8RZDl/viAA0SY5iLKoC2xbjnA45vVECLl8YOyinXN1iRZgllk2AOCI3iFzL+wbyji5SjrxrVv0Y6ZmdIePLA8HLBqrJ5Q15A66Wk0uwVHoNvhcyjuLPqtjUStWhLst+89aGX6HcxZ2//11YIYDYdHbIBZw2p9o6SfrCRO6GBJO4iAWEcgaDHwV+RTdYAIkRIuMPUTnZQljl2Ua5NeEH3Kmbm/KJesFnL3vJ5lA2CjYf8QRRBUcI30ThXKk0TZf1s6hX5Cg9FYktFIH54t1E3ruGDRAMf1gV+MmUgJFfgO4CB1y69NSX7lfemM3eHsyy8n1QEeuzx86OrJcySqybQwbGnjYw7N5o0YDS2v2GzAP0Qhbmt3sYg9CBU1PEJEwEZKNdW0K+XPFlyAot+q1DUVBK0sWkotF4TrVRkifXy+r0KspLCMJYWFJFXKFpqpdv5aJBqlF70zWmJF8mMCLaNx0XWeW90Jqd7wvVUE5VxFKErhUfgf4SFqEUHWnlq9yzu8eIbKRXgFssK4XKFmOAupP8Fz0r+RtVcXJCBkUYGhJ1ItWh5pnA9OXOwzLfy4Zqqr9XOYNqBdVctlcyS43Y56vJECtGeEJJGslZRU97WIqMFtGyK8YXPAIGhHDwJNVMiuef/EtzCbAkr8czzlBjvO7HdMdPwxATe/5/g3UaAnF2G8ismV7OU0lWu6sI6D5to4H5QgLDSh9KQ6ZW1/9LL5QxItmNPDQWWDMi/4KPY+Lm4ThFOyGDyCoPtcv9J1OHOpaxWBxah4EVA9tLfIgrKrbx7c04gq9wo2VOWSCwtRFze0kbSGweK1n+eqNqBPoR864ypcfmbJXgGisVuksjqzYhwrnwVfsofmw/Vjc4UWbVsuEMdQ2D+BRTZduQZJvWPN4sbZ3dLYNj2DDMHTCq8z3ITt07MjMuAu1axKKbAfWpD9qYC76ca0j9nRDvngm0p5gr/aZjyKGvOdoSKV2lHC3zWcGgy5RvrBOgVbZl12iexdtg/HZ8P+tahHIsZ9JjmQFWX0x+dPDhbOPVBe1UizX8Tf/8oEmtZndBD1aPbWRd9PYJ2lGPaJPWjA+aDHfUJw3cFrAXIQhSrGv3D9MY78hveR0GNrpywQPozjwcjyrjtN3iT0e+IL4B+mQkyelgNP27+0uv3gAmJzOL453HkAo4pmKEv80rXoB5upEKy84U0RPrbNIiqa+9L5cpdp7Bhe5xGT/8HMDP6lsAMDvbcswuv11hqU3sJaDlVzWw5NVMSUtIBgxzJUMvbFdEhP3p4nrv8SQg25CIGimwkLohLYLBK6RCLN2bgZw63Eg8pNqfnGX+51vw1fkyvG4aA==",
      document.getElementById("data-capture-view")!
    );
    await sdkManager.init();
  });
</script>

<main class="relative h-full">
  <div id="data-capture-view" />
</main>

<style>
  #data-capture-view {
    position: absolute;
    inset: 0;
  }

  @supports (-webkit-touch-callout: none) {
    #data-capture-view {
      height: -webkit-fill-available;
    }
  }
</style>
