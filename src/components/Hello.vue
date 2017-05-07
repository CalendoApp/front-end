<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12 col-md-3">

        <div class="left-bar">
          <div class="left-bar__profile row">
            <div class="profile">
              <img src="http://placehold.it/45" class="img-circle">
              <h4>Manu Khakulov</h4>
            </div>
          </div>

          <div class="left-bar__action row">
            <ul class="nav nav-pills nav-stacked">
              <li><a href="#">Настройки</a></li>
              <li><a href="#">Выйти</a></li>
              <hr>
              <li class="active"><a href="#">Неделя <span class="badge">42</span></a></li>
              <li><a href="#">Месяц <span class="badge">139</span></a></li>
              <li><a href="#">Год</a></li>
              <li><a href="#">Важные <span class="badge">5</span></a></li>
              <hr>
              <li>
                <div class="tag tag--red">Срочно</div>
                <div class="tag tag--blue">Работа</div>
                <div class="tag tag--red">Ебала</div>
                <div class="tag tag--blue">Всякое</div>
                <div class="tag tag--red">Быро</div>
                <div class="tag tag--blue">Хуета</div>
              </li>
            </ul>
          </div>
        </div>

      </div>
      <div class="col-xs-12 col-md-6">
        <div class="row">
          <div class="form-group">
            <input type="text" class="form-control" id="addTodo" placeholder="text">
          </div>
        </div>
        <div class="row">
          <div class="day-name"><h2>Все задачи за неделю</h2></div>

          <div class="task-item">
            <div class="task-item__check"></div>
            <div class="task-item__text">{{text}}</div>
            <div class="task-item__tags">
              <div class="tag tag--red">Срочно</div>
              <div class="tag tag--blue">Работа</div>
            </div>
          </div>

          <div class="task-item task-item--completed">
            <div class="task-item__check"></div>
            <div class="task-item__text">{{text}}</div>
            <div class="task-item__tags"></div>
          </div>

          <div class="task-item">
            <div class="task-item__check"></div>
            <div class="task-item__text">{{text}}</div>
            <div class="task-item__tags"></div>
          </div>

          <div class="task-item">
            <div class="task-item__check"></div>
            <div class="task-item__text">{{text}}</div>
            <div class="task-item__tags"></div>
          </div>

        </div>

        <div class="row">
          <div class="day-name"><h3>Понедельник, 9 мая</h3></div>

          <div class="task-item">
            <div class="task-item__check"></div>
            <div class="task-item__text">{{text}}</div>
            <div class="task-item__tags">
              <div class="tag tag--red">Срочно</div>
              <div class="tag tag--blue">Работа</div>
            </div>
          </div>

          <div class="task-item task-item--completed">
            <div class="task-item__check"></div>
            <div class="task-item__text">{{text}}</div>
            <div class="task-item__tags"></div>
          </div>

          <div class="task-item">
            <div class="task-item__check"></div>
            <div class="task-item__text">{{text}}</div>
            <div class="task-item__tags"></div>
          </div>

          <div class="task-item">
            <div class="task-item__check"></div>
            <div class="task-item__text">{{text}}</div>
            <div class="task-item__tags"></div>
          </div>

        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      text: 'Lorem ipsum dolor sit amet.'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
  @import '../assets/style/vendors/bourbon/bourbon'

  .left-bar
    &__profile
      padding: 0 20px 15px 20px
      margin-bottom: 15px

      img, h4
        display: inline-block
        vertical-align: top
      h4
        padding-top: 4px
        padding-left: 10px
    &__action
      width: 90%
      border-radius: 6px
      padding: 15px 20px
      margin-left: 2px
      background: #fff
      box-shadow: 0 0 8px 0 rgba(#000, .05)

    .badge
      float: right

  .day-name
    margin-bottom: 15px

  .task-item
    +size(100% auto)
    padding: 0 15px
    background: #fff
    box-shadow: 0 1px 3px 0 rgba(0,0,0,0.05)
    border-radius: 6px
    min-height: 50px
    line-height: 45px
    margin-bottom: 8px

    &--completed
      .task-item__text
        color: rgba(#000, .3)
        text-decoration: line-through

    &__text
      display: inline-block
      line-height: 1
      vertical-align: top
      padding: 15px 0 0 16px
      font-size: 16px

    &__check
      +size(22px)
      vertical-align: middle
      border: 2px solid rgba(#000, .15)
      border-radius: 22px
      display: inline-block

    &__tags
      display: inline-block
      line-height: 1
      padding-left: 40px
      float: right
      margin-top: 12px
      +size(auto)

  .tag
    display: inline-block
    border-radius: 4px
    font-size: 13px
    border-radius: 4px
    padding: 0 4px 0 12px
    line-height: 25px
    cursor: pointer
    vertical-align: top
    position: relative
    margin-bottom: 4px

    &:hover
      opacity: .7

    &:after
      content: '#'
      position: absolute
      left: 4px
      top: 0

    &--red
      background: #FFEBEB
      color: darken(#FFEBEB, 25%)

    &--blue
      background: #E7ECFF
      color: darken(#E7ECFF, 25%)

</style>
