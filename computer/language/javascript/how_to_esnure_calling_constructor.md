# constructor가 불리는것 보장하기. 
  * instanceof를 이용해서 new를 사용하지 않았을 때도, new의 사용을 강제할 수 있다.

        var Data = function(data1, data2) {
          if(!(this instanceof arguments.callee)) {
            return new Data(data1, data2);
          }
          this.data1 = data1;
          this.data2 = data2;
        };

        var data1 = Data("d1", "d2");
        var data2 = new Data("d3", "d4");
