```<azibai.com.core_app.ul.FontEditText
                    android:id="@+id/et$id$"
                    style="@style/textMediumHome"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:textSize="@dimen/$dimen$"
                    android:inputType="text"
                    android:background="@drawable/$bg$"
                    android:textColor="@color/$color$"
                    android:hint="@string/$string$"/>


<androidx.appcompat.widget.AppCompatImageView
            android:id="@+id/iv$id$"
            android:layout_width="@dimen/_20dp"
            android:layout_height="@dimen/_20dp"
            android:scaleType="centerCrop"
            android:src="@drawable/ic_$drawable$"
      />

<androidx.recyclerview.widget.RecyclerView
        android:id="@+id/rv$id$"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        app:layoutManager="androidx.recyclerview.widget.LinearLayoutManager" />



<azibai.com.core_app.ul.FontTextView
            android:id="@+id/tv$id$"
            style="@style/textMediumHome"
            android:textColor="@color/$color$"
            android:textSize="@dimen/$dimen$"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            tools:text="" />

<View
        android:id="@+id/vTop"
        android:background="@color/gray5"
        app:layout_constraintBottom_toBottomOf="parent"
        android:layout_width="match_parent"
        android:layout_height="1dp"/>



class $NAME$Adapter(inflater: LayoutInflater, loadMore: Fun, val clickItem: Fun1<$MODEL$>) :
    EndlessLoadAdapter<$MODEL$>(inflater, $MODEL$(), loadMore) {
    override fun onCreateHolder(parent: ViewGroup, viewType: Int): BaseHolder<$MODEL$> {
        return object :
            BaseHolder<$MODEL$>(inflater.inflate($LAYOUT_ID$, parent, false)) {
            init {
                itemView.setOnClickListener{
                    clickItem.invoke(dataSource[adapterPosition])
                }
            }

            override fun bind(data: $MODEL$, position: Int) {
               
            }
        }
    }
}




class $NAME$Binder(var onClickItem: Fun1<$MODEL$>) : ItemBinder<$MODEL$, ItemHolder<$MODEL$>>() {
    override fun createViewHolder(parent: ViewGroup?): ItemHolder<$MODEL$> {
        return object : ItemHolder<$MODEL$>(
            LayoutInflater.from(parent?.context).inflate($LAYOUT_ID$, parent, false)
        ) {
            init {
                itemView.setOnClickListener{
                    onClickItem.invoke(item)
                }
            }

            override fun bind(data: $MODEL$) {
            
            }
        }
    }

    override fun bindViewHolder(holder: ItemHolder<$MODEL$>?, item: $MODEL$?) {
        if (item != null)
            holder?.bind(item)
    }

    override fun canBindData(item: Any?): Boolean {
        return item is $MODEL$
    }
}

```
