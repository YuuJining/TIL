# Fragment
<br/>
###왜 fragment를 사용해야 할까?
>여러 개의 액티비티 안에 동일한 레이아웃이 부분적으로 추가 되어야 할 경우 프래그먼트를 사용하면 재사용이 가능하다.
>동일한 레이아웃을 사용하기 위해 코드를 복사하여 액티비티에 붙여넣기 하는 과정은 매우 좋지 않은 방법이다.

<br/>
###구성
>프래그먼트를 위한 XML 레이아웃과 소스 파일이 한 쌍으로 만들어진다.

<br/>

* fragment.java
<pre>
<code>
public class fragment extends Fragment {
  @Nullable
  @Override
  public View onCreateView(LayoutInflater inflater, @Nullable ViewGroup container, @Nullable Bundle savedInstanceState) {
    ViewGroup rootView = (ViewGroup) inflater.inflate(R.layout.fragment_main,container,false);

    return rootView;
  }
}
</code>
</pre>

* fragment_main.xml
<pre>
<code>
...
 < TextView
  android:layout_width="wrap_content"
  android:layout_height="wrap_content"
  android:text="Hello_world!"
   / >
...   
</code>
</pre>
<br/>
###생명주기
>프래그먼트도 액티비티처럼 수명주기(Life Cycle)가 있다. 대부분의 수명주기 메소드는 액티비티와 유사하다. 다른 점은 onAttach / onDetach 메소드가 있다.
>>onAttach는 프래그먼트가 액티비티 위에 올라갔을  호출된다.
>>onDetach는 프래그먼트가 액티비티에서 내려올 때 호출된다.

<br/>
###프래그먼트<->액티비티
>프래그먼트는 액티비티 위에 올라가 있을 때만 프래그먼트로서 동작할 수 있다.
프래그먼트에서 엑티비티의 메소드를 호출하거나 액티비티에서 프래그먼트의 메소드를 호출하면 프래그먼트와 엑티비티간에 필요한 데이터를 전달하거나 기능을 수행할 수 있다.
>>왜 메소드를 호출하는가?
>>>액티비티 간에 데이터를 전달할 때는 인텐트를 사용하는 것처럼 프래그먼트에서는 인텐트를 사용할 수 없기 때문이다.
