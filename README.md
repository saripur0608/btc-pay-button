# React BTCPay Server Pay Button

## Overview

The React BTCPay Server Pay Button is a highly customizable and easy-to-integrate component that allows you to add a BTCPay Server Pay Button to your React application. With just a few lines of code, you can enable Bitcoin payments right within your React app.

## Features

- **Easy Setup**: Just 3 easy steps to add the button to your React app.
- **Highly Customizable**: Modify button text, currency options, and more.
- **Secure**: All transactions are processed through your BTCPay Server.

## Requirements

- **BTCPay Server**: You must have access to a BTCPay Server, either self-hosted or through a third-party in order to handle payments.
- **React Application**: This component is intended to be used within an existing React application.

## Installation

### Manual Installation

1. Run `npm install react-btcpay-paybutton` to install the package into your React project.
2. Follow the steps below to add the `ReactBtcPayButton` component to your app.

## Quick Start

Here's how you can add the React BTCPay Server Pay Button to your application:

### Step 1: Import the Component

```jsx
import { ReactBtcPayButton } from 'react-btcpay-paybutton';
```

### Step 2: Add Component to Your App

To integrate the React BTCPay Button into your application, simply include it in your JSX as shown below (with optional settings):

```jsx
<ReactBtcPayButton
  // REQUIRED
  btcPayDomain='yourserver.com' // BTCPay Server Domain (example: yourserver.com)
  storeId='yourstoreid' // BTCPay Server Store ID
  currency='SATS' // Default currency for dropdown 
  currencyOptions={['SATS']} // Comma-separated values for dropdown: 'BTC', 'USD', 'EUR', etc.
  defaultPaymentMethod='SATS' // Payment method to use: 'BTC', 'SATS'
  mode='Fixed' // Form Options: 'Fixed', 'Custom', 'Slider'
  inputMin={1} // Input field minimum (SATS)
  inputMax={21000000000000} // Input field maximum (SATS)
  sliderMin={1} // Slider minimum (SATS)
  sliderMax={250000} // Slider maximum (SATS)
  submitBtnText='Pay with' // Submit button text
  showImage={false} // Show the BTCPay Server logo in the button? {true} or {false}
  // OPTIONAL
  imageSize='' //  BTCPay Server logo height. Default options: '40px', '46px', or '57px'
  checkoutDesc='' // Checkout description. Example: 'Thank your for your payment!'
  orderId='' // Order ID. Example: '0001'
  serverIpn='' // Server IPN. Example: 'https://your-server-ipn.com'
  notifyEmail='' // Notification email address. Example: 'your-email@example.com'
  browserRedirect='' // Browser redirect URL. Example: 'https://your-redirect.com'
/>

```

### Step 3: Customize Settings and Design

The `ReactBtcPayButton` component accepts various props that allow you to customize its behavior and appearance. Below are detailed explanations for each of these props:

- **`btcPayDomain`**:  
  The domain where your BTCPay Server is hosted. Replace this with your BTCPay Server domain. This is a required field.

- **`storeId`**:  
  The ID of your store on the BTCPay Server. Replace this with your specific store ID. This is a required field.

- **`currency`**:  
  Specifies the default currency you would like to use for payments. The default value is `'SATS'`. This is a required field.

- **`currencyOptions`**:  
  An array that defines the set of currencies that you can add to the dropdown. For example, you can set it to `['BTC', 'USD']` to enable Bitcoin and U.S. Dollar as options. This is a required field.

- **`defaultPaymentMethod`**:  
  Specifies the payment method that should be pre-selected when the component loads. For example, setting this to `'SATS'` would make Lightning Network the initially selected payment method. This is a required field.

- **`mode`**:  
  The display mode of the BTCPay form. Select: 'Fixed', 'Custom', or 'Slider'. This is a required field.

- **`inputMin`**:  
  Specifies the minimum amount that can be entered in the input field. This is a required field.

- **`inputMax`**:  
  Specifies the maximum amount that can be entered in the input field. This is a required field.

- **`sliderMin`**:  
  Specifies the minimum value for the payment slider. This is a required field.

- **`sliderMax`**:  
  Specifies the maximum value for the payment slider. This is a required field.

- **`submitBtnText`**:  
  The text displayed on the submit button. For example, setting this prop to `'Pay Now'` would change the button text to 'Pay Now'. This is a required field.

- **`showImage`**:  
  Choose to show or hide the button image. Options: {true} or {false} This is a required field.

- **`imageSize`**:  
  Specifies the height for the button image (BTCPay Server logo). Defaults: 40px, 46px, 57px

- **`checkoutDesc`**:  
  The description that appears on the checkout invoice. You can use this field to describe the product or service you are offering.

- **`orderId`**:  
  An identifier for the order. This can be useful for keeping track of transactions.

- **`serverIpn`**:  
  The URL of the server where Instant Payment Notifications (IPN) will be sent. The server must be capable of handling POST requests.

- **`notifyEmail`**:  
  The email address where notifications about the transaction will be sent.

- **`browserRedirect`**:  
  The URL to which the browser will be redirected after the payment process is completed or cancelled.

## Documentation

For more detailed information and advanced customization options, please refer to the [BTCPay Server Documentation](https://docs.btcpayserver.org/) and [React Documentation](https://legacy.reactjs.org/docs/getting-started.html).

## Contributing

Feel free to report issues, suggest features, and submit pull requests.

## Acknowledgements

Thank you to the teams behind React and BTCPay Server for providing the essential tools and frameworks used in this project.

## License

This project is open-source and available under the MIT License.