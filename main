from flask import Flask, jsonify, request

app = Flask(__name__)

# Root route for sanity check
@app.route('/')
def home():
    return "PulseBot is running!", 200

# Sample API route
@app.route('/api/message', methods=['POST'])
def handle_message():
    data = request.json
    message = data.get('message', '')
    
    # Example logic (Echo back for now)
    response = {
        'response': f'You said: {message}'
    }
    return jsonify(response)

if __name__ == '__main__':
    app.run(debug=True)
