<template>
  <div class="max-w-md mx-auto p-4">
    <form @submit.prevent="sendSMS" class="space-y-4">
      <div>
        <label for="phoneNumber" class="block">Phone Number:</label>
        <input type="text" id="phoneNumber" v-model="phoneNumber"
          class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:border-blue-500">
      </div>
      <div>
        <label for="message" class="block">Message:</label>
        <textarea id="message" v-model="message"
          class="w-full border border-gray-300 rounded-md p-2 focus:outline-none focus:border-blue-500"></textarea>
      </div>
      <button type="submit" class="w-full bg-blue-500 text-white py-2 rounded-md hover:bg-blue-600">Send SMS</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const phoneNumber = ref('');
const message = ref('');

const sendSMS = async () => {
  const accountSid = 'ACba08b2719baecf0c5495d79ba3a5c649';
  const authToken = '7fed163eec4d944d6b1bc962907e01c6';

  if (process.client) { // Ensure Twilio is imported only on the client side
    const twilio = await import('twilio');
    // Initialize Twilio client
    const client = twilio.default(accountSid, authToken);
    try {
      // Send the SMS message
      await client.messages.create({
        body: message.value,
        from: '+16267225024',
        to: phoneNumber.value
      });
      alert('SMS sent successfully!');
    } catch (error) {
      console.error('Error sending SMS:', error);
      alert('Failed to send SMS. Please try again later.');
    }
  }
};
</script>