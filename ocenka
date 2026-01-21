import streamlit as st
import pandas as pd


st.title("Любими плодове – класна анкета")

if "colors" not in st.session_state:
    st.session_state.colors = {
        "Ябълка": 0,
        "Банан": 0,
        "Портокал": 0,
        "Грозде": 0
    }


color = st.selectbox(
    "Любим плод:",
    list(st.session_state.colors.keys())
)


if st.button("Запази избора"):
    st.session_state.colors[color] += 1


colors_df = pd.DataFrame.from_dict(
    st.session_state.colors,
    orient="index",
    columns=["Брой"]
)

# Показване на графика
st.bar_chart(colors_df)
