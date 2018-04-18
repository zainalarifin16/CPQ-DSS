$(document)
    .ready(function () {

        if (navigator.userAgent.match(/Android/i)
            || navigator.userAgent.match(/webOS/i)
            || navigator.userAgent.match(/iPhone/i)
            || navigator.userAgent.match(/iPad/i)
            || navigator.userAgent.match(/iPod/i)
            || navigator.userAgent.match(/BlackBerry/i)
            || navigator.userAgent.match(/Windows Phone/i)
        ) {
            $('.ui.sidebar')
                .sidebar('attach events', '.toc.item');

            if (window.innerWidth < 768){

                var header = [];

                $(".ui.table").find("thead th").map(function(index, data){
                    header.push($(data).html());
                });

                $(".ui.table").find("tr").map(function (index, tr) {
                    
                    $(tr).css("min-height", "170px");

                    var td = $(tr).find("td");
                    var date = td[0];
                    var orderNo = td[1];
                    var ezrxNo = td[2];
                    var saleId = td[3];
                    var shippingId = td[4];
                    var companyName = td[5];
                    var status = td[6];
                    var action = td[7];

                    //styling
                    $(date).css({"float": "left"});
                    $(status).css({"float": "right"});
                    $(companyName).attr("style", "float:left; width: 100%!important; text-align: left; font-size: 18px; padding-left: 10px!important;");
                    $(orderNo).attr("style", "float:left;width: 50%!important;text-align: left;");
                    $(saleId).attr("style", "float:left;width: 50%!important;text-align: left;");
                    $(shippingId).attr("style", "float:left;width: 50%!important;text-align: left;");
                    $(action).css({"float": "right"});

                    //moving object
                    $(ezrxNo).attr("style", "display: none!important;");
                    $(orderNo).before( status );
                    $(orderNo).before( companyName );
                    $(orderNo).before($("<td>Order No.</td>").attr("style", "float:left;width: 30%!important;text-align:left;"));
                    $(saleId).before($("<td>Sale Id.</td>").attr("style", "float:left;width: 30%!important;text-align:left;") );
                    $(shippingId).before($("<td>Shipping Id.</td>").attr("style", "float:left;width: 30%!important;text-align:left;") );
                });
            }
        }
    });