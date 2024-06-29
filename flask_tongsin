from flask import Flask, request, jsonify

app = Flask(__name__)

# /test 경로에 POST 요청 처리
@app.route('/test', methods=['POST'])
def test_endpoint():
    # 클라이언트가 보낸 JSON 데이터 받기
    request_data = request.json
    
    # 요청이 없거나 key가 없으면 400 에러 반환
    if not request_data or 'key' not in request_data:
        return jsonify({'error': 'Invalid request'}), 400
    
    # 요청 처리 후 응답 반환
    response_data = {'key': 'test OK'}
    return jsonify(response_data)

# /test2 경로에 GET 요청 처리
@app.route('/test2', methods=['GET'])
def test2_endpoint():
    # 요청 처리 후 응답 반환
    response_data = {'test': 'OK'}
    return jsonify(response_data)

if __name__ == '__main__':
    app.run(debug=True)
    
