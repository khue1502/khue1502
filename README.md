describe('Test code được tạo ra cho chính mình', () => {
    before(() => {
        require('expect-webdriverio').setOptions({ wait: 5000 });
    });
    it('Truy cập google.com.vn và nhập từ khóa tìm kiếm', () => {
        browser.url('https://www.google.com.vn');
        $('input[type="text"]').addValue('automation testing');
        browser.keys('\uE00C');
        $('input[type="submit"]').click();
        $('*=Automation Testing').click();
        expect(browser).toHaveTitleContaining('Automation Testing');
    });
});
