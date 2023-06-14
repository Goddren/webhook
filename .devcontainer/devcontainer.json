from flask import Flask, request

app = Flask(__name__)

@app.route('/webhook', methods=['POST'])
def webhook():
    data = request.get_json()  # Get the JSON data from the request payload
    
    # Retrieve the desired inputs from the webhook data or request parameters
    alert_type = data.get('alert_type')  # Example: Retrieve the alert type from the webhook data
    
    # Process the webhook data and perform your desired actions using the inputs
    if alert_type == 'buy':
        # Set up logic for placing a buy order
        # Example: place_buy_order()
        print("Buy order placed.")
    elif alert_type == 'sell':
        # Set up logic for placing a sell order
        # Example: place_sell_order()
        print("Sell order placed.")
    else:
        # Handle other alert types or errors
        print("Unknown alert type:", alert_type)
    
    # Example: Print the received webhook data and the extracted alert type
    print("Received Webhook Data:")
    print(data)
    print("Alert Type:", alert_type)
    
    # Return a response to acknowledge the webhook
    return 'Webhook received successfully'

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
