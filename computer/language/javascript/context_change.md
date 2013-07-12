# context 바꾸기

  * call 혹은 apply로 제공한 object를 함수 내에서 this로 받는다.

        var context1 = {};
        var context2 = {};
        var s = function(n, a) { this[n] = a; };
        var g = function(n) { return this[n]; };
        s.call(context1, "a", 10);
        s.call(context2, "a", 20);
        g.call(context1, "a");     //10
        g.call(context2, "a");     //20
        // or
        s.apply(context1, ["a", 30]);
        s.apply(context2, ["a", 40]);
        g.apply(context1, ["a"]);  //30
        g.apply(context2, ["a"]);  //40
