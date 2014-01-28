if (typeof Object.create !== 'function') {
    Object.create = function (obj) {
        function F() { };
        F.prototype = obj;
        return new F();
    };
}

(function ($, window, document, undefined) {
    var Twitter = {
        init: function (options, elem) {
            var self = this ;
            self.elem = elem;
            self.$elem = $(elem);
            self.options = $.extend({}, $.fn.pluginName.options, options);
            self.refresh(1);
        },
        refresh: function (length) {
            var self = this ;
        }
    };

    $.fn.queryTwitter = function (options) {
        return this .each(function () {
            var twitter = Object.create(Twitter);
            twitter.init(options, this);
            $.data( this, 'queryTwitter' , twitter);
        });
    };

    $.fn.pluginName.options = {
        search: '@tutspremium',
        wrapEachWith: '<li></li>',
        limit: 10,
        refresh: null,
        onComplete: null,
        transition: 'fadeToggle'
    };

})(jQuery, window, document);

