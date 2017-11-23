<template>
    <div class="nav">
        <nav>
            <div>Menu</div>
            <ul>
                <li>
                    <a href="#" title="1">1<img src="img/down.png" class="more" alt="down"></a>
                    <ul class="sub_nav">
                        <li><a href="#" title="2">2</a></li>
                        <li><a href="#" title="3">3</a></li>
                    </ul>
                </li>
                <li><a href="#" title="4">4</a></li>
                <li><a href="#" title="5">5</a></li>                
            </ul>        
        </nav>
	</div>
</template>

<script>
export default {
    // 특별한 함수 설정 없이 사용하고 싶은데 오류가 나는 상황입니다. 
    $('nav > ul > li').click(function(){
        $('nav > ul > li').removeClass('nav_sel');
        $(this).addClass('nav_sel');
        $('.more').attr('src', 'img/down.png');
        $('.more', this).attr('src', 'img/up.png');

        if(!$('.nav_sel').children().hasClass('sub_nav')){
            $(this).css('padding-bottom', '12px');  
        };
    });

    $('.sub_nav > li').click(function(){
        $('.sub_nav > li').removeClass('sub_nav_sel');
        $(this).addClass('sub_nav_sel');
    });
}
</script>

<style scoped>

</style>
