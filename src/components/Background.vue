<template>
  <div id="back">
    N<p></p>
    <p>UT</p>
    <p>FE</p>
    <p>&nbsp;S</p>
  </div>
</template>

<script>
export default {
  name: 'Background',
};
</script>

<style lang="scss">
  @mixin stripes($direction, $colors) {
    $length: length($colors);

    @if $length > 1 {
      $stripes: ();
      $stripe: 0;
      @for $i from 1 through $length {
        @if $i == 1 or $i == $length + 1 {
          $stripe: $stripe;
        }@else if $i % 2 == 0 {
          $stripe: $stripe + 20%;
        } @else {
          $stripe: $stripe + 5%;
        }

        @if $i > 1 {
          $previous-color: nth($colors, $i - 1);
          $stripes: append($stripes, $previous-color $stripe, comma);
          }

        $stripes: append($stripes, nth($colors, $i) $stripe, comma);

      }
      background: linear-gradient($direction, $stripes) fixed;
    } @else if $length == 1 {
      background-color: $colors;
    }
  }

  body {
    @include stripes(to bottom, #87cedd #f5f5f5 #adff2f #f5f5f5 #ffdf00 #f5f5f5 #ff6347 #f5f5f5)
  }

  #back {
    text-align: left;
    color: #fffacd;
    font-size: 450%;
  }

</style>
