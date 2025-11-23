<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover, maximum-scale=5.0, user-scalable=yes">
    <meta name="description" content="가상계좌 관리 시스템 - 고객/관리자 통합 플랫폼">
    <meta name="keywords" content="가상계좌, 계좌관리, 대출, 신청, 관리자, 금융">
    <meta name="author" content="Korea Federation of Banks">
    <meta name="theme-color" content="#667eea">
    <meta name="color-scheme" content="light dark">

    <!-- Apple Mobile Web App Meta Tags -->
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="가상계좌 관리">
    <meta name="apple-touch-icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 180 180'><rect fill='%23667eea' width='180' height='180'/><text x='50%' y='50%' font-size='100' text-anchor='middle' dominant-baseline='central' font-family='system-ui' font-weight='bold' fill='white'>🏦</text></svg>">
    <meta name="apple-touch-icon-precomposed" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 180 180'><rect fill='%23667eea' width='180' height='180'/><text x='50%' y='50%' font-size='100' text-anchor='middle' dominant-baseline='central' font-family='system-ui' font-weight='bold' fill='white'>🏦</text></svg>">

    <!-- Windows/Android Meta Tags -->
    <meta name="msapplication-TileColor" content="#667eea">
    <meta name="msapplication-config" content="browserconfig.xml">
    <meta name="format-detection" content="telephone=no">
    <meta name="format-detection" content="email=no">

    <!-- Open Graph (Social Media) Meta Tags -->
    <meta property="og:type" content="website">
    <meta property="og:title" content="가상계좌 관리 시스템 - 고객/관리자 통합">
    <meta property="og:description" content="효율적인 가상계좌 관리 및 대출 신청 플랫폼">
    <meta property="og:url" content="https://virtual-account.example.com">
    <meta property="og:image" content="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1200 630'><rect fill='%23667eea' width='1200' height='630'/><text x='600' y='300' font-size='120' text-anchor='middle' dominant-baseline='central' font-family='system-ui' font-weight='bold' fill='white'>🏦 가상계좌 관리</text></svg>">
    <meta property="og:site_name" content="가상계좌 관리 시스템">

    <!-- Twitter Card Meta Tags -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="가상계좌 관리 시스템">
    <meta name="twitter:description" content="효율적인 가상계좌 관리 및 대출 신청 플랫폼">

    <!-- Additional Mobile Meta Tags -->
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="HandheldFriendly" content="true">
    <meta name="MobileOptimized" content="width">
    <meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

    <title>가상계좌 관리 시스템 - 고객/관리자 통합</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }

        /* ===== 로그인 화면 ===== */
        .login-container {
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            padding: 20px;
        }

        .login-box {
            background: white;
            padding: 50px;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
            max-width: 450px;
            width: 100%;
        }

        .login-header {
            text-align: center;
            margin-bottom: 40px;
        }

        .login-logo {
            font-size: 48px;
            margin-bottom: 15px;
        }

        .login-title {
            font-size: 28px;
            font-weight: 700;
            color: #1e3c72;
            margin-bottom: 10px;
        }

        .login-subtitle {
            font-size: 14px;
            color: #999;
        }

        .role-selector {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 25px;
        }

        .role-btn {
            padding: 15px;
            border: 2px solid #ddd;
            background: white;
            border-radius: 10px;
            cursor: pointer;
            font-weight: 600;
            font-size: 16px;
            transition: all 0.3s;
            text-align: center;
        }

        .role-btn:hover {
            border-color: #667eea;
            color: #667eea;
        }

        .role-btn.active {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-color: #667eea;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #1e3c72;
            font-size: 14px;
        }

        .form-group input {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 14px;
            transition: border-color 0.3s;
        }

        .form-group input:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102,126,234,0.1);
        }

        .login-button {
            width: 100%;
            padding: 13px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            font-size: 16px;
            cursor: pointer;
            transition: transform 0.3s;
            margin-top: 10px;
        }

        .login-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102,126,234,0.4);
        }

        .demo-credentials {
            background: #f5f7ff;
            padding: 15px;
            border-radius: 8px;
            font-size: 12px;
            color: #666;
            margin-top: 20px;
            border-left: 4px solid #667eea;
        }

        /* ===== 메인 콘텐츠 ===== */
        .app-container {
            display: none;
            min-height: 100vh;
        }

        .app-container.active {
            display: flex;
            flex-direction: column;
        }

        /* 헤더 */
        header {
            background: white;
            padding: 15px 30px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .header-left {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .logo {
            font-size: 24px;
            font-weight: bold;
            color: #1e3c72;
        }

        .role-badge {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
        }

        .role-badge.customer {
            background: linear-gradient(135deg, #4caf50 0%, #45a049 100%);
        }

        .role-badge.admin {
            background: linear-gradient(135deg, #ff9800 0%, #f57c00 100%);
        }

        .header-right {
            display: flex;
            align-items: center;
            gap: 20px;
        }

        .user-info {
            text-align: right;
            font-size: 13px;
            color: #666;
        }

        .user-info .name {
            font-weight: 600;
            color: #1e3c72;
        }

        .logout-btn {
            padding: 8px 20px;
            background: #f0f0f0;
            border: 2px solid #ddd;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 600;
            font-size: 13px;
            transition: all 0.3s;
        }

        .logout-btn:hover {
            background: #e74c3c;
            color: white;
            border-color: #e74c3c;
        }

        /* 컨테이너 */
        .container {
            flex: 1;
            max-width: 1400px;
            margin: 0 auto;
            padding: 30px 20px;
            width: 100%;
        }

        /* 탭 네비게이션 */
        .tab-navigation {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
            background: white;
            padding: 0;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .tab-btn {
            flex: 1;
            padding: 15px;
            background: white;
            border: none;
            cursor: pointer;
            font-size: 14px;
            font-weight: 600;
            color: #999;
            transition: all 0.3s;
            border-bottom: 3px solid transparent;
        }

        .tab-btn.active {
            color: #667eea;
            border-bottom-color: #667eea;
            background: #f5f7ff;
        }

        .tab-btn:hover {
            color: #667eea;
            background: #f9f9f9;
        }

        /* 탭 컨텐츠 */
        .tab-content {
            display: none;
            animation: fadeIn 0.3s;
        }

        .tab-content.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* 카드 */
        .card {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            margin-bottom: 20px;
        }

        .card-title {
            font-size: 18px;
            font-weight: 700;
            color: #1e3c72;
            margin-bottom: 20px;
            padding-bottom: 15px;
            border-bottom: 2px solid #f0f0f0;
        }

        /* 폼 */
        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 20px;
        }

        .form-group {
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-weight: 600;
            color: #1e3c72;
            margin-bottom: 8px;
            font-size: 14px;
        }

        .form-group label .required {
            color: #e74c3c;
            margin-left: 3px;
        }

        .form-group input,
        .form-group select,
        .form-group textarea {
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 14px;
            font-family: inherit;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group select:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102,126,234,0.1);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 100px;
        }

        /* 버튼 */
        .button-group {
            display: flex;
            gap: 10px;
            justify-content: flex-end;
            margin-top: 25px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 12px 30px;
            border: none;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            font-size: 14px;
            transition: all 0.3s;
        }

        .btn-primary {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102,126,234,0.4);
        }

        .btn-secondary {
            background: #f0f0f0;
            color: #333;
        }

        .btn-secondary:hover {
            background: #e0e0e0;
        }

        .btn-small {
            padding: 8px 15px;
            font-size: 12px;
        }

        /* 테이블 */
        .table-wrapper {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            overflow-x: auto;
            margin-bottom: 20px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 13px;
        }

        thead {
            background: #f5f7ff;
        }

        th {
            padding: 15px;
            text-align: left;
            font-weight: 600;
            color: #1e3c72;
            border-bottom: 2px solid #ddd;
        }

        td {
            padding: 15px;
            border-bottom: 1px solid #eee;
        }

        tbody tr:hover {
            background: #f9f9f9;
        }

        /* 상태 배지 */
        .status-badge {
            display: inline-block;
            padding: 6px 12px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
        }

        .status-pending {
            background: #fff3cd;
            color: #856404;
        }

        .status-approved {
            background: #d4edda;
            color: #155724;
        }

        .status-rejected {
            background: #f8d7da;
            color: #721c24;
        }

        /* 통계 카드 */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 15px;
            margin-bottom: 20px;
        }

        .stat-card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }

        .stat-label {
            font-size: 13px;
            color: #999;
            margin-bottom: 10px;
        }

        .stat-value {
            font-size: 28px;
            font-weight: 700;
            color: #667eea;
        }

        /* 알림 */
        .alert {
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
            display: none;
            border-left: 4px solid;
        }

        .alert.active {
            display: block;
        }

        .alert.success {
            background: #d4edda;
            color: #155724;
            border-color: #28a745;
        }

        .alert.error {
            background: #f8d7da;
            color: #721c24;
            border-color: #f5c6cb;
        }

        /* 모달 */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
        }

        .modal.active {
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background: white;
            padding: 40px;
            border-radius: 12px;
            max-width: 500px;
            width: 90%;
            box-shadow: 0 10px 40px rgba(0,0,0,0.3);
        }

        .modal-header {
            font-size: 20px;
            font-weight: 700;
            color: #1e3c72;
            margin-bottom: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .close-btn {
            font-size: 24px;
            color: #999;
            cursor: pointer;
            background: none;
            border: none;
        }

        /* 승인 모달 */
        #approvalModal {
            display: none;
        }

        #approvalModal.active {
            display: flex;
        }

        /* 반응형 */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }

            .login-box {
                padding: 30px 20px;
            }

            .form-grid {
                grid-template-columns: 1fr;
            }

            .button-group {
                justify-content: center;
            }

            header {
                flex-direction: column;
                gap: 15px;
            }

            .tab-btn {
                font-size: 12px;
                padding: 12px;
            }

            table {
                font-size: 11px;
            }

            th, td {
                padding: 10px;
            }
        }

        /* 고객 전용 스타일 */
        .customer-info {
            background: linear-gradient(135deg, #e8f5e9 0%, #f1f8e9 100%);
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
            border-left: 4px solid #4caf50;
        }

        .customer-info h3 {
            color: #2e7d32;
            margin-bottom: 10px;
        }

        /* 숨기기 클래스 */
        .hidden {
            display: none !important;
        }
    </style>
</head>
<body>

<!-- ===== 로그인 화면 ===== -->
<div id="loginScreen" class="login-container">
    <div class="login-box">
        <div class="login-header">
            <div class="login-logo">🏦</div>
            <div class="login-title">가상계좌 관리</div>
            <div class="login-subtitle">고객/관리자 통합 시스템</div>
        </div>

        <div class="role-selector">
            <button class="role-btn active" onclick="selectRole('customer')">
                👤 고객
            </button>
            <button class="role-btn" onclick="selectRole('admin')">
                👨‍💼 관리자
            </button>
        </div>

        <form onsubmit="handleLogin(event)">
            <div class="form-group">
                <label>아이디</label>
                <input type="text" id="loginId" required placeholder="아이디 입력">
            </div>

            <div class="form-group">
                <label>비밀번호</label>
                <input type="password" id="loginPassword" required placeholder="비밀번호 입력">
            </div>

            <button type="submit" class="login-button">로그인</button>
        </form>

        <div class="demo-credentials">
            <strong>📋 개인정보 처리방침</strong><br>
            <span style="font-size: 11px; color: #666;">
                [04538] 서울특별시 중구 명동11길 19 (명동1가 4-1)<br>
                대표전화 : 02-3705-5000<br>
                Copyright 2006 Korea Federation of Banks. All rights reserved.
            </span>
        </div>
    </div>
</div>

<!-- ===== 메인 앱 ===== -->
<div id="appContainer" class="app-container">
    <!-- 헤더 -->
    <header>
        <div class="header-left">
            <div class="logo">🏦 가상계좌 관리</div>
            <div class="role-badge" id="roleBadge">고객</div>
        </div>
        <div class="header-right">
            <div class="user-info">
                <div class="name" id="displayName">사용자</div>
                <div id="displayTime">현재시간</div>
            </div>
            <button class="logout-btn" onclick="handleLogout()">로그아웃</button>
        </div>
    </header>

    <!-- 컨테이너 -->
    <div class="container">
        <div id="alertMessage" class="alert"></div>

        <!-- ===== 고객 페이지 ===== -->
        <div id="customerPage" class="hidden">
            <!-- 탭 -->
            <div class="tab-navigation">
                <button class="tab-btn active" onclick="switchTab('customer-application')">📝 신청하기</button>
                <button class="tab-btn" onclick="switchTab('customer-status')">📊 신청현황</button>
                <button class="tab-btn" onclick="switchTab('customer-account')">💳 계좌정보</button>
            </div>

            <!-- 신청하기 탭 -->
            <div id="customer-application" class="tab-content active">
                <div class="card">
                    <div class="card-title">가상계좌 신청</div>
                    <form id="customerApplicationForm" onsubmit="submitCustomerApplication(event)">
                        <div class="form-grid">
                            <div class="form-group">
                                <label>이름 <span class="required">*</span></label>
                                <input type="text" id="custName" required>
                            </div>

                            <div class="form-group">
                                <label>휴대폰 <span class="required">*</span></label>
                                <input type="tel" id="custPhone" required placeholder="010-0000-0000">
                            </div>

                            <div class="form-group">
                                <label>납입금액 (만원) <span class="required">*</span></label>
                                <input type="number" id="custLoanAmount" required min="0">
                            </div>

                            <div class="form-group">
                                <label>납부목적 <span class="required">*</span></label>
                                <input type="text" id="custPaymentPurpose" required placeholder="예: 학비, 의료비">
                            </div>

                            <div class="form-group" style="grid-column: 1 / -1;">
                                <label>용도 <span class="required">*</span></label>
                                <select id="custPurpose" required>
                                    <option value="">선택해주세요</option>
                                    <option value="대환">대환</option>
                                    <option value="기타">기타</option>
                                </select>
                            </div>
                        </div>

                        <div class="button-group">
                            <button type="button" class="btn btn-secondary" onclick="resetCustomerForm()">초기화</button>
                            <button type="submit" class="btn btn-primary">신청하기</button>
                        </div>
                    </form>
                </div>
            </div>

            <!-- 신청현황 탭 -->
            <div id="customer-status" class="tab-content">
                <div class="card">
                    <div class="card-title">내 신청현황</div>
                    <div class="table-wrapper">
                        <table>
                            <thead>
                                <tr>
                                    <th>신청번호</th>
                                    <th>납입금액</th>
                                    <th>납부목적</th>
                                    <th>용도</th>
                                    <th>상태</th>
                                    <th>신청일</th>
                                    <th>작업</th>
                                </tr>
                            </thead>
                            <tbody id="customerApplicationsTable">
                                <tr>
                                    <td colspan="7" style="text-align: center; color: #999;">신청 내역이 없습니다</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>

            <!-- 계좌정보 탭 -->
            <div id="customer-account" class="tab-content">
                <div class="card">
                    <div class="customer-info">
                        <h3>💳 당신의 가상계좌</h3>
                        <p id="customerVirtualAccount" style="font-size: 14px; margin-top: 10px;">
                            <strong>계좌번호:</strong> <span style="font-family: monospace; font-weight: bold; color: #1e3c72;">-</span>
                        </p>
                        <p style="font-size: 12px; color: #555; margin-top: 15px;">
                            ⚠️ 계좌는 신청 승인 후에 발급됩니다
                        </p>
                    </div>
                </div>
            </div>
        </div>

        <!-- ===== 관리자 페이지 ===== -->
        <div id="adminPage">
            <!-- 탭 -->
            <div class="tab-navigation">
                <button class="tab-btn active" onclick="switchTab('admin-dashboard')">📊 대시보드</button>
                <button class="tab-btn" onclick="switchTab('admin-applications')">📝 신청관리</button>
                <button class="tab-btn" onclick="switchTab('admin-verification')">✓ 인증관리</button>
                <button class="tab-btn" onclick="switchTab('admin-transfer')">💸 이체관리</button>
            </div>

            <!-- 대시보드 탭 -->
            <div id="admin-dashboard" class="tab-content active">
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-label">총 신청 건수</div>
                        <div class="stat-value" id="adminTotalApps">0</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-label">대기 중</div>
                        <div class="stat-value" id="adminPendingApps">0</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-label">승인됨</div>
                        <div class="stat-value" id="adminApprovedApps">0</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-label">총 대출액</div>
                        <div class="stat-value" id="adminTotalLoan">0</div>
                    </div>
                </div>
            </div>

            <!-- 신청관리 탭 -->
            <div id="admin-applications" class="tab-content">
                <div class="card">
                    <div class="card-title">신청 관리</div>
                    <div class="table-wrapper">
                        <table>
                            <thead>
                                <tr>
                                    <th>신청번호</th>
                                    <th>신청자</th>
                                    <th>연락처</th>
                                    <th>금액(만원)</th>
                                    <th>상태</th>
                                    <th>신청일</th>
                                    <th>작업</th>
                                </tr>
                            </thead>
                            <tbody id="adminApplicationsTable">
                                <tr>
                                    <td colspan="7" style="text-align: center; color: #999;">신청 데이터가 없습니다</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>

            <!-- 인증관리 탭 -->
            <div id="admin-verification" class="tab-content">
                <div class="card">
                    <div class="card-title">가상계좌 인증 관리</div>
                    <div class="form-grid">
                        <div class="form-group">
                            <label>신청번호 검색</label>
                            <input type="text" id="adminSearchId" placeholder="APP-2024001">
                        </div>
                        <div class="button-group" style="grid-column: 1 / -1;">
                            <button class="btn btn-primary" onclick="adminSearchApplication()">검색</button>
                        </div>
                    </div>

                    <div id="adminVerificationResult" style="display: none; margin-top: 20px;">
                        <div style="background: #e3f2fd; padding: 15px; border-radius: 8px; border-left: 4px solid #667eea;">
                            <strong>📱 인증번호:</strong>
                            <div style="font-size: 24px; font-weight: bold; color: #667eea; margin: 10px 0; letter-spacing: 3px; font-family: monospace;" id="adminAuthCode">000000</div>
                            <button class="btn btn-primary btn-small" onclick="copyAuthCode()">복사</button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 이체관리 탭 -->
            <div id="admin-transfer" class="tab-content">
                <div class="card">
                    <div class="card-title">대출금 이체</div>
                    <form id="adminTransferForm" onsubmit="submitAdminTransfer(event)">
                        <div class="form-grid">
                            <div class="form-group">
                                <label>신청자 계좌 <span class="required">*</span></label>
                                <input type="text" id="adminTransferAccount" required placeholder="110-123456789">
                            </div>

                            <div class="form-group">
                                <label>수취인명 <span class="required">*</span></label>
                                <input type="text" id="adminTransferReceiver" required>
                            </div>

                            <div class="form-group">
                                <label>수취인 계좌 <span class="required">*</span></label>
                                <input type="text" id="adminTransferReceiverAccount" required>
                            </div>

                            <div class="form-group">
                                <label>은행명 <span class="required">*</span></label>
                                <select id="adminTransferBank" required>
                                    <option value="">선택해주세요</option>
                                    <option value="국민은행">국민은행</option>
                                    <option value="우리은행">우리은행</option>
                                    <option value="신한은행">신한은행</option>
                                    <option value="하나은행">하나은행</option>
                                    <option value="농협">농협</option>
                                </select>
                            </div>

                            <div class="form-group">
                                <label>이체금액 (만원) <span class="required">*</span></label>
                                <input type="number" id="adminTransferAmount" required min="0">
                            </div>

                            <div class="form-group">
                                <label>이체일자 <span class="required">*</span></label>
                                <input type="date" id="adminTransferDate" required>
                            </div>
                        </div>

                        <div class="button-group">
                            <button type="button" class="btn btn-secondary" onclick="resetAdminTransferForm()">초기화</button>
                            <button type="submit" class="btn btn-primary">이체 실행</button>
                        </div>
                    </form>
                </div>

                <div class="card" style="margin-top: 30px;">
                    <div class="card-title">이체 내역</div>
                    <div class="table-wrapper">
                        <table>
                            <thead>
                                <tr>
                                    <th>이체번호</th>
                                    <th>신청자계좌</th>
                                    <th>수취인</th>
                                    <th>금액(만원)</th>
                                    <th>은행</th>
                                    <th>이체일</th>
                                </tr>
                            </thead>
                            <tbody id="adminTransferTable">
                                <tr>
                                    <td colspan="6" style="text-align: center; color: #999;">이체 내역이 없습니다</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<!-- 승인 모달 -->
<div id="approvalModal" class="modal">
    <div class="modal-content">
        <div class="modal-header">
            <span>가상계좌 발급</span>
            <button class="close-btn" onclick="closeApprovalModal()">×</button>
        </div>
        
        <div style="margin-bottom: 20px; padding: 15px; background: #f5f7ff; border-radius: 8px; border-left: 4px solid #667eea;">
            <p style="font-size: 13px; color: #666;">
                <strong>신청자:</strong> <span id="approvalAppName">-</span><br>
                <strong>신청번호:</strong> <span id="approvalAppNo">-</span><br>
                <strong>신청금액:</strong> <span id="approvalAppAmount">-</span>만원
            </p>
        </div>

        <form onsubmit="submitApproval(event)">
            <div class="form-group">
                <label>가상계좌번호 <span class="required">*</span></label>
                <input type="text" id="approvalVirtualAccount" required placeholder="예) 110-123456789 또는 110-12345678901 (11~16자리)" autofocus>
            </div>

            <div class="form-group">
                <label>은행명 <span class="required">*</span></label>
                <input type="text" id="approvalBank" required placeholder="국민은행" autofocus>
            </div>

            <div class="form-group">
                <label>계좌보유자명</label>
                <input type="text" id="approvalAccountHolder" placeholder="선택사항">
            </div>

            <div class="button-group" style="justify-content: flex-end; margin-top: 20px;">
                <button type="button" class="btn btn-secondary" onclick="closeApprovalModal()">취소</button>
                <button type="submit" class="btn btn-primary">승인 및 발급</button>
            </div>
        </form>
    </div>
</div>

<script>
    // ===== 전역 변수 =====
    let currentUser = null;
    let currentRole = 'customer';
    let applications = JSON.parse(localStorage.getItem('applications')) || [];
    let transfers = JSON.parse(localStorage.getItem('transfers')) || [];

    // 데모 계정
    const demoAccounts = {
        customer: {
            'user1': '1234',
            'user2': '1234'
        },
        admin: {
            'admin': 'admin123'
        }
    };

    // ===== 로그인 관련 =====
    function selectRole(role) {
        currentRole = role;
        document.querySelectorAll('.role-btn').forEach(btn => btn.classList.remove('active'));
        event.target.classList.add('active');
    }

    function handleLogin(event) {
        event.preventDefault();
        const id = document.getElementById('loginId').value;
        const password = document.getElementById('loginPassword').value;

        if (!id || !password) {
            alert('❌ 아이디와 비밀번호를 모두 입력해주세요.');
            return;
        }

        const validPassword = demoAccounts[currentRole]?.[id];
        
        if (!validPassword) {
            alert('❌ 존재하지 않는 아이디입니다.\n\n데모 계정:\n고객: user1 / 1234\n관리자: admin / admin123');
            return;
        }

        if (validPassword !== password) {
            alert('❌ 비밀번호가 일치하지 않습니다.');
            return;
        }

        currentUser = {
            id: id,
            role: currentRole,
            name: currentRole === 'admin' ? '관리자 ' + id : '고객 ' + id
        };

        showApp();
    }

    function showApp() {
        document.getElementById('loginScreen').style.display = 'none';
        document.getElementById('appContainer').classList.add('active');

        // 사용자 정보 표시
        document.getElementById('displayName').textContent = currentUser.name;
        
        const badge = document.getElementById('roleBadge');
        if (currentUser.role === 'admin') {
            badge.textContent = '👨‍💼 관리자';
            badge.classList.add('admin');
            badge.classList.remove('customer');
            document.getElementById('customerPage').classList.add('hidden');
            document.getElementById('adminPage').classList.remove('hidden');
            updateAdminDashboard();
        } else {
            badge.textContent = '👤 고객';
            badge.classList.add('customer');
            badge.classList.remove('admin');
            document.getElementById('customerPage').classList.remove('hidden');
            document.getElementById('adminPage').classList.add('hidden');
            updateCustomerStatus();
        }

        updateTime();
        setInterval(updateTime, 1000);
    }

    function handleLogout() {
        if (confirm('로그아웃하시겠습니까?')) {
            currentUser = null;
            document.getElementById('appContainer').classList.remove('active');
            document.getElementById('loginScreen').style.display = 'flex';
            document.getElementById('loginId').value = '';
            document.getElementById('loginPassword').value = '';
        }
    }

    // ===== 시간 표시 =====
    function updateTime() {
        const now = new Date();
        document.getElementById('displayTime').textContent = now.toLocaleTimeString('ko-KR');
    }

    // ===== 탭 전환 =====
    function switchTab(tabName) {
        // 모든 탭 숨기기
        document.querySelectorAll('.tab-content').forEach(tab => {
            tab.classList.remove('active');
        });
        
        // 모든 버튼 비활성화
        document.querySelectorAll('.tab-btn').forEach(btn => {
            btn.classList.remove('active');
        });

        // 선택 탭 활성화
        const tabElement = document.getElementById(tabName);
        if (tabElement) {
            tabElement.classList.add('active');
            event.target.classList.add('active');
        }
    }

    // ===== 고객 기능 =====
    function submitCustomerApplication(event) {
        event.preventDefault();

        const appData = {
            appNo: 'APP-' + Date.now(),
            virtualAccount: '110-' + Math.floor(Math.random() * 900000 + 100000) + '-' + Math.floor(Math.random() * 900000 + 100000),
            customerName: document.getElementById('custName').value,
            phone: document.getElementById('custPhone').value,
            paymentAmount: document.getElementById('custLoanAmount').value,
            paymentPurpose: document.getElementById('custPaymentPurpose').value,
            purpose: document.getElementById('custPurpose').value,
            status: '대기',
            customerId: currentUser.id,
            applicationDate: new Date().toLocaleString('ko-KR')
        };

        applications.push(appData);
        localStorage.setItem('applications', JSON.stringify(applications));

        showAlert('success', '✓ 신청이 완료되었습니다. 곧 연락드리겠습니다.');
        document.getElementById('customerApplicationForm').reset();

        setTimeout(() => {
            updateCustomerStatus();
            switchTab('customer-status');
        }, 1500);
    }

    function resetCustomerForm() {
        document.getElementById('customerApplicationForm').reset();
    }

    function updateCustomerStatus() {
        const myApps = applications.filter(app => app.customerId === currentUser.id);
        const tbody = document.getElementById('customerApplicationsTable');

        if (myApps.length === 0) {
            tbody.innerHTML = '<tr><td colspan="7" style="text-align: center; color: #999;">신청 내역이 없습니다</td></tr>';
            document.getElementById('customerVirtualAccount').innerHTML = '<strong>계좌번호:</strong> <span style="font-family: monospace; font-weight: bold; color: #1e3c72;">-</span>';
            return;
        }

        tbody.innerHTML = myApps.map(app => `
            <tr>
                <td><strong>${app.appNo}</strong></td>
                <td>${app.paymentAmount}만원</td>
                <td>${app.paymentPurpose}</td>
                <td>${app.purpose}</td>
                <td><span class="status-badge status-${app.status === '대기' ? 'pending' : app.status === '승인' ? 'approved' : 'rejected'}">${app.status}</span></td>
                <td>${app.applicationDate}</td>
                <td><button class="btn btn-small btn-secondary" onclick="copyAppNo('${app.appNo}')">복사</button></td>
            </tr>
        `).join('');

        // 승인된 계좌 표시
        const approvedApp = myApps.find(app => app.status === '승인');
        if (approvedApp) {
            document.getElementById('customerVirtualAccount').innerHTML = `<strong>계좌번호:</strong> <span style="font-family: monospace; font-weight: bold; color: #1e3c72;">${approvedApp.virtualAccount}</span>`;
        }
    }

    function copyAppNo(appNo) {
        navigator.clipboard.writeText(appNo);
        showAlert('success', '✓ 신청번호가 복사되었습니다.');
    }

    // ===== 관리자 기능 =====
    function updateAdminDashboard() {
        const total = applications.length;
        const pending = applications.filter(app => app.status === '대기').length;
        const approved = applications.filter(app => app.status === '승인').length;
        const totalLoan = applications.reduce((sum, app) => sum + parseInt(app.loanAmount || 0), 0);

        document.getElementById('adminTotalApps').textContent = total;
        document.getElementById('adminPendingApps').textContent = pending;
        document.getElementById('adminApprovedApps').textContent = approved;
        document.getElementById('adminTotalLoan').textContent = totalLoan.toLocaleString();

        updateAdminApplicationsTable();
    }

    function updateAdminApplicationsTable() {
        const tbody = document.getElementById('adminApplicationsTable');

        if (applications.length === 0) {
            tbody.innerHTML = '<tr><td colspan="7" style="text-align: center; color: #999;">신청 데이터가 없습니다</td></tr>';
            return;
        }

        tbody.innerHTML = applications.map(app => `
            <tr>
                <td><strong>${app.appNo}</strong></td>
                <td>${app.customerName}</td>
                <td>${app.phone}</td>
                <td>${app.loanAmount}</td>
                <td><span class="status-badge status-${app.status === '대기' ? 'pending' : app.status === '승인' ? 'approved' : 'rejected'}">${app.status}</span></td>
                <td style="font-size: 12px;">${app.applicationDate}</td>
                <td>
                    ${app.status === '대기' ? `<button class="btn btn-small btn-primary" onclick="adminApproveApp('${app.appNo}')">승인</button>` : ''}
                    <button class="btn btn-small btn-secondary" onclick="adminDeleteApp('${app.appNo}')" style="margin-left: 5px;">삭제</button>
                </td>
            </tr>
        `).join('');
    }

    function adminApproveApp(appNo) {
        const app = applications.find(a => a.appNo === appNo);
        if (!app) return;

        // 모달에 정보 표시
        document.getElementById('approvalAppName').textContent = app.customerName;
        document.getElementById('approvalAppNo').textContent = app.appNo;
        document.getElementById('approvalAppAmount').textContent = app.loanAmount;
        document.getElementById('approvalVirtualAccount').value = '';
        document.getElementById('approvalBank').value = '국민은행';
        document.getElementById('approvalAccountHolder').value = '';

        // 현재 앱번호 저장
        sessionStorage.setItem('currentApprovalAppNo', appNo);

        // 모달 열기
        document.getElementById('approvalModal').classList.add('active');
    }

    function closeApprovalModal() {
        document.getElementById('approvalModal').classList.remove('active');
        sessionStorage.removeItem('currentApprovalAppNo');
    }

    function submitApproval(event) {
        event.preventDefault();

        const appNo = sessionStorage.getItem('currentApprovalAppNo');
        const virtualAccount = document.getElementById('approvalVirtualAccount').value.trim();
        const bankName = document.getElementById('approvalBank').value.trim();
        const accountHolder = document.getElementById('approvalAccountHolder').value.trim();

        if (!virtualAccount) {
            alert('❌ 가상계좌번호를 입력해주세요.');
            return;
        }

        if (!bankName) {
            alert('❌ 은행명을 입력해주세요.');
            return;
        }

        // 계좌 형식 검증 (11~16자리 숫자 + 하이픈)
        // 예시: 110-123456789, 110-12345678901, 110-123456789-12345 등
        const accountNumber = virtualAccount.replace(/-/g, '');
        if (!/^\d{11,16}$/.test(accountNumber)) {
            alert('❌ 계좌번호는 11자리 이상 16자리 이하의 숫자여야 합니다.\n예시: 110-123456789 또는 110-12345678901');
            return;
        }

        const app = applications.find(a => a.appNo === appNo);
        if (app) {
            app.status = '승인';
            app.virtualAccount = virtualAccount;
            app.bankName = bankName;
            app.accountHolder = accountHolder || '미입력';
            app.approvalDate = new Date().toLocaleString('ko-KR');

            localStorage.setItem('applications', JSON.stringify(applications));
            updateAdminDashboard();
            showAlert('success', `✓ ${appNo}이(가) 승인되었습니다.\n계좌: ${bankName} ${virtualAccount}`);
            closeApprovalModal();
        }
    }

    function adminDeleteApp(appNo) {
        if (!confirm('정말 삭제하시겠습니까?')) return;
        applications = applications.filter(app => app.appNo !== appNo);
        localStorage.setItem('applications', JSON.stringify(applications));
        updateAdminDashboard();
        showAlert('success', '✓ 삭제되었습니다.');
    }

    function adminSearchApplication() {
        const searchId = document.getElementById('adminSearchId').value.trim();
        
        if (!searchId) {
            showAlert('error', '❌ 신청번호를 입력해주세요.');
            return;
        }

        const app = applications.find(a => a.appNo === searchId);
        if (!app) {
            showAlert('error', '❌ 일치하는 신청이 없습니다.');
            document.getElementById('adminVerificationResult').style.display = 'none';
            return;
        }

        const authCode = String(Math.floor(Math.random() * 900000 + 100000));
        document.getElementById('adminAuthCode').textContent = authCode;
        document.getElementById('adminVerificationResult').style.display = 'block';
    }

    function copyAuthCode() {
        const authCode = document.getElementById('adminAuthCode').textContent;
        navigator.clipboard.writeText(authCode);
        showAlert('success', '✓ 인증번호가 복사되었습니다.');
    }

    function submitAdminTransfer(event) {
        event.preventDefault();

        const transferData = {
            transferNo: 'TR-' + Date.now(),
            accountNo: document.getElementById('adminTransferAccount').value,
            receiver: document.getElementById('adminTransferReceiver').value,
            receiverAccount: document.getElementById('adminTransferReceiverAccount').value,
            bank: document.getElementById('adminTransferBank').value,
            amount: document.getElementById('adminTransferAmount').value,
            date: document.getElementById('adminTransferDate').value,
            timestamp: new Date().toLocaleString('ko-KR')
        };

        transfers.push(transferData);
        localStorage.setItem('transfers', JSON.stringify(transfers));

        showAlert('success', '✓ 이체가 완료되었습니다.');
        document.getElementById('adminTransferForm').reset();
        updateAdminTransferTable();
    }

    function resetAdminTransferForm() {
        document.getElementById('adminTransferForm').reset();
    }

    function updateAdminTransferTable() {
        const tbody = document.getElementById('adminTransferTable');

        if (transfers.length === 0) {
            tbody.innerHTML = '<tr><td colspan="6" style="text-align: center; color: #999;">이체 내역이 없습니다</td></tr>';
            return;
        }

        tbody.innerHTML = transfers.map(tr => `
            <tr>
                <td><strong>${tr.transferNo}</strong></td>
                <td style="font-family: monospace; font-size: 12px;">${tr.accountNo}</td>
                <td>${tr.receiver}</td>
                <td>${tr.amount}</td>
                <td>${tr.bank}</td>
                <td>${tr.date}</td>
            </tr>
        `).join('');
    }

    // ===== 알림 =====
    function showAlert(type, message) {
        const alert = document.getElementById('alertMessage');
        alert.textContent = message;
        alert.className = `alert active ${type}`;

        setTimeout(() => {
            alert.classList.remove('active');
        }, 3000);
    }

    // 초기 로드
    document.addEventListener('DOMContentLoaded', () => {
        updateAdminTransferTable();
        
        // 모달 바깥 클릭 시 닫기
        document.getElementById('approvalModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closeApprovalModal();
            }
        });
    });
</script>

</body>
</html>
