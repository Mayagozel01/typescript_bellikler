#### ts taze owrenip bashlanlar un ts tiplerinin hakyky tejribede ulanylyshyndan bir bolek


```
import type { Product } from "../types";


export const SET_PRODUCTS = 'SET_PRODUCTS';
export const ADD_PRODUCT =  'ADD_PRODUCT';
export const REMOVE_PRODUCT =  'REMOVE_PRODUCT';
// barde literal tip duzulen, yagny ts-de sheydip uytgeyja setir yazanymyzda ol setiri tip diyip kabul edya.


interface SetProductsAction {
    type: typeof SET_PRODUCTS;
    payload : Product[];
}
// interface obyekti we onun duzumini beyan edyar
// barde SetProductsAction obyekt bolup onun duzuminde type diyen hasiyet we ol hasiyeting bahasy SET_PRODUCTS bolmaly.
// payload bolsa Product obyektin massivi bolmaly

interface AddProductAction {
    type: typeof ADD_PRODUCT;
    payload: Product;
}
(*barde payload Product diylen obyekt bolmaly  *)

interface RemoveProductAction {
    type: typeof REMOVE_PRODUCT;
    payload: number;
}

export type ProductActionTypes = SetProductsAction | AddProductAction | RemoveProductAction;

(* bu bolsa union diyilyan tip, barde shu ProductActionTypes arasy "|" bolunen 3 tipin islendik biri bp biler   *)


export const setProducts = (products:Product[]):SetProductsAction=>({
   type: SET_PRODUCTS,
   payload: products, 
})


export const addProduct = (product:Product):AddProductAction=>({
    type: ADD_PRODUCT,
    payload: product,
})


export const removeProduct = (id:number):RemoveProductAction=>({
    type: REMOVE_PRODUCT,
    payload:id,
})
```
